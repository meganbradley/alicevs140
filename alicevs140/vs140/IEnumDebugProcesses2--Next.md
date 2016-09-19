---
title: "IEnumDebugProcesses2::Next"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: abef89eb-198b-49cd-a4c9-17bce6cac0e1
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugProcesses2::Next
Returns the next set of elements from the enumeration.  
  
## Syntax  
  
```cpp#  
HRESULT Next(  
   ULONG            celt,  
   IDebugProcess2** rgelt,  
   ULONG*           pceltFetched  
);  
```  
  
```c#  
int Next(  
   uint             celt,  
   IDebugProcess2[] rgelt,  
   ref uint         pceltFetched  
);  
```  
  
#### Parameters  
 `celt`  
 [in] The number of elements to retrieve. Also specifies the maximum size of the `rgelt` array.  
  
 `rgelt`  
 [in, out] Array of [IDebugProcess2](../vs140/IDebugProcess2.md) elements to be filled in.  
  
 `pceltFetched`  
 [out] Returns the number of elements actually returned in `rgelt`.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if fewer than the requested number of elements could be returned; otherwise, returns an error code.  
  
## See Also  
 [IEnumDebugProcesses2](../vs140/IEnumDebugProcesses2.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)