---
title: "lock_guard::~lock_guard Destructor"
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
ms.assetid: e8d62d7b-6c13-44b2-866d-0ee10763db36
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# lock_guard::~lock_guard Destructor
Unlocks the `mutex` that was passed to the constructor.  
  
## Syntax  
  
```  
~lock_guard() _NOEXCEPT;  
```  
  
## Remarks  
 If the `mutex` does not exist when the destructor runs, the behavior is undefined.  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
## See Also  
 [lock_guard Class](../vs140/lock_guard-Class.md)   
 [<mutex\>](../vs140/-mutex-.md)