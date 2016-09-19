---
title: "SRWLock::TryLockExclusive Method"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 661e8b19-3058-4511-8742-c9fbb90412c7
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SRWLock::TryLockExclusive Method
Attempts to acquire a SRWLock object in exclusive mode for the current or specified SRWLock object. If the call is successful, the calling thread takes ownership of the lock.  
  
## Syntax  
  
```  
SyncLockExclusive TryLockExclusive();  
  
static SyncLockExclusive TryLockExclusive(  
   _In_ SRWLOCK* lock  
);  
```  
  
#### Parameters  
 `lock`  
 Pointer to an SRWLock object.  
  
## Return Value  
 If successful, an SRWLock object in exclusive mode and the calling thread takes ownership of the lock. Otherwise, an SRWLock object whose state is invalid.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [SRWLock Class](../vs140/SRWLock-Class.md)