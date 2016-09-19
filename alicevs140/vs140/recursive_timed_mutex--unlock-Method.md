---
title: "recursive_timed_mutex::unlock Method"
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
ms.topic: article
ms.assetid: 6b4ebf63-7b88-4c97-829f-8a14eb9aa297
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# recursive_timed_mutex::unlock Method
Releases ownership of the `mutex`.  
  
## Syntax  
  
```cpp  
void unlock();  
```  
  
## Remarks  
 This method releases ownership of the `mutex` only after it is called as many times as [lock](../vs140/recursive_timed_mutex--lock-Method.md), [try_lock](../vs140/recursive_timed_mutex--try_lock-Method.md), [try_lock_for](../vs140/recursive_timed_mutex--try_lock_for-Method.md), and [try_lock_until](../vs140/recursive_timed_mutex--try_lock_until-Method.md) have been called successfully on the `recursive_timed_mutex` object.  
  
 If the calling thread does not own the `mutex`, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)   
 [recursive_timed_mutex Class](../vs140/recursive_timed_mutex-Class.md)