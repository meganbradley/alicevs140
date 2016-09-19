---
title: "IDebugBreakpointBoundEvent2::GetPendingBreakpoint"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6da7ed86-b412-4964-b6a3-0687a66f63fe
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointBoundEvent2::GetPendingBreakpoint
Gets the pending breakpoint that is being bound.  
  
## Syntax  
  
```cpp#  
HRESULT GetPendingBreakpoint(   
   IDebugPendingBreakpoint2** ppPendingBP  
);  
```  
  
```cpp#  
int GetPendingBreakpoint(   
   out IDebugPendingBreakpoint2 ppPendingBP  
);  
```  
  
#### Parameters  
 `ppPendingBP`  
 [out] Returns the [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md) object that represents the pending breakpoint being bound.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Example  
 The following example shows how to implement this method for a **CBreakpointSetDebugEventBase** object that exposes the [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md) interface.  
  
```cpp#  
STDMETHODIMP CBreakpointSetDebugEventBase::GetPendingBreakpoint(  
    IDebugPendingBreakpoint2 **ppPendingBP)  
{  
    HRESULT hRes = E_FAIL;  
  
    if ( ppPendingBP )  
    {  
        if ( m_pPendingBP )  
        {  
            *ppPendingBP = m_pPendingBP;  
  
            m_pPendingBP->AddRef();  
  
            hRes = S_OK;  
        }  
        else  
            hRes = E_FAIL;  
    }  
    else  
        hRes = E_INVALIDARG;  
  
    return ( hRes );  
}  
```  
  
## See Also  
 [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)