---
title: "IDebugReference2::GetReferenceInfo"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ae611714-f114-4cf2-b5bb-37461e6ff289
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugReference2::GetReferenceInfo
Gets the [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structure that describes a reference. Reserved for future use.  
  
## Syntax  
  
```cpp#  
HRESULT GetReferenceInfo (   
   DEBUGREF_INFO_FLAGS   dwFields,  
   DWORD                 nRadix,  
   DWORD                 dwTimeout,  
   IDebugReference2**    rgpArgs,  
   DWORD                 dwArgCount,  
   DEBUG_REFERENCE_INFO* pReferenceInfo  
);  
```  
  
```c#  
int GetReferenceInfo (   
   enum_DEBUGREF_INFO_FLAGS  dwFields,  
   uint                      nRadix,  
   uint                      dwTimeout,  
   IDebugReference2[]        rgpArgs,  
   uint                      dwArgCount,  
   DEBUG_REFERENCE_INFO[]    pReferenceInfo  
);  
```  
  
#### Parameters  
 `dwFields`  
 [in] A combination of flags from the [DEBUGREF_INFO_FLAGS](../vs140/DEBUGREF_INFO_FLAGS.md) enumeration that determine the fields to be filled out in the [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structure.  
  
 `nRadix`  
 [in] The radix to be used in formatting any numerical information.  
  
 `dwTimeout`  
 [in] Maximum time, in milliseconds, to wait before returning from this method. Use `INFINITE` to wait indefinitely.  
  
 `rgpArgs`  
 [in] An array of [IDebugReference2](../vs140/IDebugReference2.md) objects. Reserved for future use; set to a null value.  
  
 `dwArgCount`  
 [in] The number of reference arguments in the `rgpArgs` array. Reserved for future use; set to 0.  
  
 `pReferenceInfo`  
 [out] A [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) structure that is filled in with a description of the property.  
  
## Return Value  
 Always returns `E_NOTIMPL`.  
  
## See Also  
 [IDebugReference2](../vs140/IDebugReference2.md)   
 [DEBUGREF_INFO_FLAGS](../vs140/DEBUGREF_INFO_FLAGS.md)   
 [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md)