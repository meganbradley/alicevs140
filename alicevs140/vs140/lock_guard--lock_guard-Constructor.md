---
title: "lock_guard::lock_guard Constructor"
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
ms.assetid: dc24c60d-c082-490b-94d7-55c817de6f89
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# lock_guard::lock_guard Constructor
Constructs a `lock_guard` object.  
  
## Syntax  
  
```cpp  
explicit lock_guard(mutex_type& Mtx);  
lock_guard(mutex_type& Mtx, adopt_lock_t);  
```  
  
#### Parameters  
 `Mtx`  
 A *mutex type* object.  
  
## Remarks  
 The first constructor constructs an object of type `lock_guard` and locks `Mtx`. If `Mtx` is not a recursive mutex, it must be unlocked when this constructor is called.  
  
 The second constructor does not lock `Mtx`. `Mtx` must be locked when this constructor is called. The constructor throws no exceptions.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [lock_guard Class](../vs140/lock_guard-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)