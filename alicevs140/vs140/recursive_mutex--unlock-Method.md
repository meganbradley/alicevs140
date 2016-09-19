---
title: "recursive_mutex::unlock Method"
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
ms.assetid: 2efc6b95-9c11-48da-b611-e22beaeb4adf
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# recursive_mutex::unlock Method
Releases ownership of the mutex.  
  
## Syntax  
  
```cpp  
void unlock();  
```  
  
## Remarks  
 This method releases ownership of the `mutex` only after it is called as many times as [lock](../vs140/recursive_mutex--lock-Method.md) and [try_lock](../vs140/recursive_mutex--try_lock-Method.md) have been called successfully on the `recursive_mutex` object.  
  
 If the calling thread does not own the `mutex`, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [recursive_mutex Class](../vs140/recursive_mutex-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)