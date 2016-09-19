---
title: "unique_lock::unlock Method"
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
ms.assetid: 489a9734-36c0-4d8b-8bbc-296f6440a47a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique_lock::unlock Method
Releases ownership of the associated `mutex`.  
  
## Syntax  
  
```cpp  
void unlock();  
```  
  
## Remarks  
 If the calling thread doesn't own the associated `mutex`, this method throws a [system_error](../vs140/system_error-Class.md) that has an error code of `operation_not_permitted`.  
  
 Otherwise, this method calls `unlock` on the associated `mutex` and sets the internal thread ownership flag to `false`.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [unique_lock Class](../vs140/unique_lock-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)