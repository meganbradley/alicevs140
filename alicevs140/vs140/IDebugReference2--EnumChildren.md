---
title: "IDebugReference2::EnumChildren"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 35b3c2f3-69f4-4013-b555-f847221f62e8
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugReference2::EnumChildren
Get a list of selected children of a reference. Reserved for future use.  
  
## Syntax  
  
```cpp#  
HRESULT EnumChildren (   
   DEBUGREF_INFO_FLAGS        dwFields,  
   DWORD                      dwRadix,  
   DBG_ATTRIB_FLAGS           dwAttribFilter,  
   LPCOLESTR                  pszNameFilter,  
   DWORD                      dwTimeout,  
   IEnumDebugReferenceInfo2** ppEnum  
);  
```  
  
```c#  
int EnumChildren (   
   enum_DEBUGREF_INFO_FLAGS     dwFields,  
   uint                         dwRadix,  
   enum_DBG_ATTRIB_FLAGS        dwAttribFilter,  
   string                       pszNameFilter,  
   uint                         dwTimeout,  
   out IEnumDebugReferenceInfo2 ppEnum  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of flags from the [DEBUGREF_INFO_FLAGS](../vs140/DEBUGREF_INFO_FLAGS.md) enumeration that specifies which fields in the enumerated [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structures are to be filled in.  
  
 `dwRadix`  
 [in] The radix to be used in formatting any numerical information.  
  
 `dwAttribFilter`  
 [in] A combination of flags from the [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md) enumeration that is used as a filter in combination with the `pszNameFilter` parameter to select which structures are to be enumerated.  
  
 `pszNameFilter`  
 [in] A string specifying a filter, such as "MyX", used in combination with the `dwAttribFilter` parameter to select the structures to be enumerated.  
  
 `dwTimeout`  
 [in] Maximum time, in milliseconds, to wait before returning from this method. Use `INFINITE` to wait indefinitely.  
  
 `ppEnum`  
 [out] Returns an [IEnumDebugReferenceInfo2](../vs140/IEnumDebugReferenceInfo2.md) object that contains a list of the requested child properties.  
  
## Return Value  
 Always returns `E_NOTIMPL`.  
  
## See Also  
 [IDebugReference2](../vs140/IDebugReference2.md)   
 [DEBUGREF_INFO_FLAGS](../vs140/DEBUGREF_INFO_FLAGS.md)   
 [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md)   
 [IEnumDebugReferenceInfo2](../vs140/IEnumDebugReferenceInfo2.md)