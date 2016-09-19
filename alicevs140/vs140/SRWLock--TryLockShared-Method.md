---
title: "SRWLock::TryLockShared Method"
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
ms.assetid: 10cc198d-39a0-4d18-aa78-706744948668
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SRWLock::TryLockShared Method
Attempts to acquire a SRWLock object in shared mode for the current or specified SRWLock object.  
  
## Syntax  
  
```  
WRL_NOTHROW SyncLockShared TryLockShared();  
WRL_NOTHROW static SyncLockShared TryLockShared(  
   _In_ SRWLOCK* lock  
);  
```  
  
#### Parameters  
 `lock`  
 Pointer to an SRWLock object.  
  
## Return Value  
 If successful, an SRWLock object in shared mode and the calling thread takes ownership of the lock. Otherwise, an SRWLock object whose state is invalid.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [SRWLock Class](../vs140/SRWLock-Class.md)