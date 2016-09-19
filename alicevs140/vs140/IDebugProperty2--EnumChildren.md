---
title: "IDebugProperty2::EnumChildren"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cf79f666-65d1-417c-af7c-9271bac9a267
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProperty2::EnumChildren
Retrieves a list of the children of the property.  
  
## Syntax  
  
```cpp#  
HRESULT EnumChildren (   
   DEBUGPROP_INFO_FLAGS      dwFields,  
   DWORD                     dwRadix,  
   REFGUID                   guidFilter,  
   DBG_ATTRIB_FLAGS          dwAttribFilter,  
   LPCOLESTR                 pszNameFilter,  
   DWORD                     dwTimeout,  
   IEnumDebugPropertyInfo2** ppEnum  
);  
```  
  
```c#  
int EnumChildren (   
   enum_DEBUGPROP_INFO_FLAGS   dwFields,  
   uint                        dwRadix,  
   ref Guid                    guidFilter,  
   uint                        dwAttribFilter,  
   string                      pszNameFilter,  
   uint                        dwTimeout,  
   out IEnumDebugPropertyInfo2 ppEnum  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of flags from the [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md) enumeration that specifies which fields in the enumerated [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structures are to be filled in.  
  
 `dwRadix`  
 [in] Specifies the radix to be used in formatting any numerical information.  
  
 `guidFilter`  
 [in] GUID of the filter used with the `dwAttribFilter` and `pszNameFilter` parameters to select which `DEBUG_PROPERTY_INFO` children are to be enumerated. For example, `guidFilterLocals` filters for local variables.  
  
 `dwAttribFilter`  
 [in] A combination of flags from the [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md) enumeration that specifies what type of objects to enumerate, for example `DBG_ATTRIB_METHOD` for all methods that might be children of this property. Used in combination with the `guidFilter` and `pszNameFilter` parameters.  
  
 `pszNameFilter`  
 [in] The name of the filter used with the `guidFilter` and `dwAttribFilter` parameters to select which `DEBUG_PROPERTY_INFO` children are to be enumerated. For example, setting this parameter to "MyX" filters for all children with the name "MyX."  
  
 `dwTimeout`  
 [in] Specifies the maximum time, in milliseconds, to wait before returning from this method. Use `INFINITE` to wait indefinitely.  
  
 `ppEnum`  
 [out] Returns an [IEnumDebugPropertyInfo2](../vs140/IEnumDebugPropertyInfo2.md) object containing a list of the child properties.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns error code.  
  
## See Also  
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md)   
 [DBG_ATTRIB_FLAGS](../vs140/DBG_ATTRIB_FLAGS.md)   
 [IEnumDebugPropertyInfo2](../vs140/IEnumDebugPropertyInfo2.md)