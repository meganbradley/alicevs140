---
title: "IEnumDebugReferenceInfo2::Next"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70b31a57-1701-4757-9e7e-63ec60a71b3c
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugReferenceInfo2::Next
Returns the next set of elements from the enumeration.  
  
## Syntax  
  
```cpp#  
HRESULT Next(  
   ULONG                   celt,  
   DEBUG_REFERENCE_INFO ** rgelt,  
   ULONG*                  pceltFetched  
);  
```  
  
```c#  
int Next(  
   uint                   celt,  
   DEBUG_REFERENCE_INFO[] rgelt,  
   ref uint               pceltFetched  
);  
```  
  
#### Parameters  
 `celt`  
 [in] The number of elements to retrieve. Also specifies the maximum size of the `rgelt` array.  
  
 `rgelt`  
 [in, out] Array of [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md) elements to be filled in.  
  
 `pceltFetched`  
 [out] Returns the number of elements actually returned in `rgelt`.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if fewer than the requested number of elements could be returned; otherwise, returns an error code.  
  
## See Also  
 [IEnumDebugReferenceInfo2](../vs140/IEnumDebugReferenceInfo2.md)   
 [DEBUG_REFERENCE_INFO](../vs140/DEBUG_REFERENCE_INFO.md)