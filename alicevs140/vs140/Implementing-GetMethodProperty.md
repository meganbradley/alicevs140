---
title: "Implementing GetMethodProperty"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6305874f-a2c4-4432-834c-07530ea84bff
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Implementing GetMethodProperty
> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Visual Studio calls the debug engine's (DE) [IDebugStackFrame2::GetDebugProperty](../vs140/IDebugStackFrame2--GetDebugProperty.md), which in turn calls [IDebugExpressionEvaluator::GetMethodProperty](../vs140/IDebugExpressionEvaluator--GetMethodProperty.md) to obtain information about the current method on the stack frame.  
  
 This implementation of `IDebugExpressionEvaluator::GetMethodProperty` performs the following tasks:  
  
1.  Calls [IDebugSymbolProvider::GetContainerField](../vs140/IDebugSymbolProvider--GetContainerField.md), passing in the [IDebugAddress](../vs140/IDebugAddress.md) object. The symbol provider (SP) returns an [IDebugContainerField](../vs140/IDebugContainerField.md) representing the method that contains the specified address.  
  
2.  Obtains the [IDebugMethodField](../vs140/IDebugMethodField.md) from the `IDebugContainerField`.  
  
3.  Instantiates a class (called `CFieldProperty` in this example) that implements the [IDebugProperty2](../vs140/IDebugProperty2.md) interface and contains the `IDebugMethodField` object returned from the SP.  
  
4.  Returns the `IDebugProperty2` interface from the `CFieldProperty` object.  
  
## Managed Code  
 This example shows an implementation of `IDebugExpressionEvaluator::GetMethodProperty` in managed code.  
  
```c#  
namespace EEMC  
{  
    [GuidAttribute("462D4A3D-B257-4AEE-97CD-5918C7531757")]  
    public class EEMCClass : IDebugExpressionEvaluator  
    {  
        public HRESULT GetMethodProperty(  
                IDebugSymbolProvider symbolProvider,  
                IDebugAddress        address,  
                IDebugBinder         binder,  
                int                  includeHiddenLocals,  
            out IDebugProperty2      property)   
        {  
            IDebugContainerField containerField = null;  
            IDebugMethodField methodField       = null;  
            property = null;  
  
            // Get the containing method field.  
            symbolProvider.GetContainerField(address, out containerField);  
            methodField = (IDebugMethodField) containerField;  
  
            // Return the property of method field.  
            property = new CFieldProperty(symbolProvider, address, binder, methodField);  
            return COM.S_OK;  
        }  
    }  
}  
```  
  
## Unmanaged Code  
 This example shows an implementation of `IDebugExpressionEvaluator::GetMethodProperty` in unmanaged code.  
  
```  
[CPP]  
STDMETHODIMP CExpressionEvaluator::GetMethodProperty(  
        in IDebugSymbolProvider *pprovider,  
        in IDebugAddress        *paddress,  
        in IDebugBinder         *pbinder,  
        in BOOL                  includeHiddenLocals,  
        out IDebugProperty2    **ppproperty  
    )  
{  
    if (pprovider == NULL)  
        return E_INVALIDARG;  
  
    if (ppproperty == NULL)  
        return E_INVALIDARG;  
    else  
        *ppproperty = 0;  
  
    HRESULT hr;  
    IDebugContainerField* pcontainer = NULL;  
  
    hr = pprovider->GetContainerField(paddress, &pcontainer);  
    if (FAILED(hr))  
        return hr;  
  
    IDebugMethodField*    pmethod    = NULL;  
    hr = pcontainer->QueryInterface( IID_IDebugMethodField,  
            reinterpret_cast<void**>(&pmethod));  
    pcontainer->Release();  
    if (FAILED(hr))  
        return hr;  
  
    CFieldProperty* pfieldProperty = new CFieldProperty( pprovider,  
                                                         paddress,  
                                                         pbinder,  
                                                         pmethod );  
    pmethod->Release();  
    if (!pfieldProperty)  
        return E_OUTOFMEMORY;  
  
    hr = pfieldProperty->Init();  
    if (FAILED(hr))  
    {  
        pfieldProperty->Release();  
        return hr;  
    }  
  
    hr = pfieldProperty->QueryInterface( IID_IDebugProperty2,  
            reinterpret_cast<void**>(ppproperty));  
    pfieldProperty->Release();  
  
    return hr;  
}  
```  
  
## See Also  
 [Sample Implementation of Locals](../vs140/Sample-Implementation-of-Locals.md)