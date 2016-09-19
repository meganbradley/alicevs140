---
title: "IEnumDebugThreads2::Next"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bcffd954-3c67-4867-96f3-041ddb3e34d4
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugThreads2::Next
Returns the next set of elements from the enumeration.  
  
## Syntax  
  
```cpp#  
HRESULT Next(  
   ULONG           celt,  
   IDebugThread2** rgelt,  
   ULONG*          pceltFetched  
);  
```  
  
```c#  
int Next(  
   uint            celt,  
   IDebugThread2[] rgelt,  
   ref uint        pceltFetched  
);  
```  
  
#### Parameters  
 `celt`  
 [in] The number of elements to retrieve. Also specifies the maximum size of the `rgelt` array.  
  
 `rgelt`  
 [in, out] Array of [IDebugThread2](../vs140/IDebugThread2.md) elements to be filled in.  
  
 `pceltFetched`  
 [out] Returns the number of elements actually returned in `rgelt`.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if fewer than the requested number of elements could be returned; otherwise, returns an error code.  
  
## See Also  
 [IEnumDebugThreads2](../vs140/IEnumDebugThreads2.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)