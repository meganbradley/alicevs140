---
title: "SimpleClassFactory::CreateInstance Method"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 17b7947a-2608-49d9-b730-fef76501c9bc
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SimpleClassFactory::CreateInstance Method
Creates an instance of the specified interface.  
  
## Syntax  
  
```  
  
STDMETHOD(  
   CreateInstance  
)  
   (_Inout_opt_ IUnknown* pUnkOuter,   
   REFIID riid,   
   _Deref_out_ void** ppvObject);  
```  
  
#### Parameters  
 `pUnkOuter`  
 Must be `nullptr`; otherwise, the return value is CLASS_E_NOAGGREGATION.  
  
 SimpleClassFactory doesn't support aggregation. If aggregation were supported and the object being created was part of an aggregate, `pUnkOuter` would be a pointer to the controlling IUnknown interface of the aggregate.  
  
 `riid`  
 Interface ID of the object to create.  
  
 `ppvObject`  
 When this operation completes, pointer to an instance of the object specified by the `riid` parameter.  
  
## Return Value  
 S_OK if successful; otherwise, an HRESULT that indicates the error.  
  
## Remarks  
 If __WRL_STRICT\_\_ is defined, an assert error is emitted if the base class specified in the class template parameter isn't derived from [RuntimeClass](../vs140/RuntimeClass-Class.md), or isn't configured with the ClassicCom or WinRtClassicComMix [RuntimeClassType](../vs140/RuntimeClassType-Enumeration.md) enumeration value.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [SimpleClassFactory Class](../vs140/SimpleClassFactory-Class.md)