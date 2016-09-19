---
title: "IDebugProperty2::GetPropertyInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 39d6e942-df72-4c84-a5d9-a386d112714c
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProperty2::GetPropertyInfo
Gets the [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structure that describes a property.  
  
## Syntax  
  
```cpp#  
HRESULT GetPropertyInfo (   
   DEBUGPROP_INFO_FLAGS dwFields,  
   DWORD                nRadix,  
   DWORD                dwTimeout,  
   IDebugReference2**   rgpArgs,  
   DWORD                dwArgCount,  
   DEBUG_PROPERTY_INFO* pPropertyInfo  
);  
```  
  
```cpp#  
int GetPropertyInfo (   
   enum_DEBUGPROP_INFO_FLAGS dwFields,  
   uint                      nRadix,  
   uint                      dwTimeout,  
   IDebugReference2[]        rgpArgs,  
   uint                      dwArgCount,  
   DEBUG_PROPERTY_INFO[]     pPropertyInfo  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of values from the [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md) enumeration that specifies which fields are to be filled out in the `pPropertyInfo` structure.  
  
 `nRadix`  
 [in] Radix to be used in formatting any numerical information.  
  
 `dwTimeout`  
 [in] Specifies the maximum time, in milliseconds, to wait before returning from this method. Use `INFINITE` to wait indefinitely.  
  
 `rgpArgs`  
 [in, out] Reserved for future use; set to a null value.  
  
 `dwArgCount`  
 [in] Reserved for future use; set to zero.  
  
 `pPropertyInfo`  
 [out] A [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md) structure that is filled in with the description of the property.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns error code.  
  
## See Also  
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [DEBUGPROP_INFO_FLAGS](../vs140/DEBUGPROP_INFO_FLAGS.md)   
 [IDebugReference2](../vs140/IDebugReference2.md)   
 [DEBUG_PROPERTY_INFO](../vs140/DEBUG_PROPERTY_INFO.md)