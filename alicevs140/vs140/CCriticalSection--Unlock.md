---
title: "CCriticalSection::Unlock"
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
ms.assetid: 63d2a94b-8417-4586-80c0-af4f1a0a1766
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCriticalSection::Unlock
Releases the `CCriticalSection` object for use by another thread.  
  
## Syntax  
  
```  
  
BOOL Unlock( );  
  
```  
  
## Return Value  
 Nonzero if the `CCriticalSection` object was owned by the thread and the release was successful; otherwise 0.  
  
## Remarks  
 If the `CCriticalSection` is being used stand-alone, `Unlock` must be called immediately after completing use of the resource controlled by the critical section. If a [CSingleLock](../vs140/CSingleLock-Class.md) object is being used, `CCriticalSection::Unlock` will be called by the lock object's `Unlock` member function.  
  
## Example  
 See the example for [CCriticalSection::Lock](../vs140/CCriticalSection--Lock.md).  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CCriticalSection Class](../vs140/CCriticalSection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)