---
title: "IDebugReference2::SetValueAsReference"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 94a545d2-16b9-45e9-b2e7-4e49ff90aad0
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugReference2::SetValueAsReference
Sets the value of a reference from another reference. Reserved for future use.  
  
## Syntax  
  
```cpp#  
HRESULT SetValueAsReference (   
   IDebugReference2** rgpArgs,  
   DWORD              dwArgCount,  
   IDebugReference2*  pValue,  
   DWORD              dwTimeout  
);  
```  
  
```cpp#  
int SetValueAsReference (   
   IDebugReference2[] rgpArgs,  
   uint               dwArgCount,  
   IDebugReference2   pValue,  
   uint               dwTimeout  
);  
```  
  
#### Parameters  
 `rgpArgs`  
 [in] An array of [IDebugReference2](../vs140/IDebugReference2.md) objects used to determine how to set the reference value.  
  
 `dwArgCount`  
 [in] The number of references in the array.  
  
 `pValue`  
 [in] An [IDebugReference2](../vs140/IDebugReference2.md) object from which to set the property value.  
  
 `dwTimeout`  
 [in] Maximum time, in milliseconds, to wait before returning from this method. Use `INFINITE` to wait indefinitely.  
  
## Return Value  
 Always returns `E_NOTIMPL`.  
  
## See Also  
 [IDebugReference2](../vs140/IDebugReference2.md)