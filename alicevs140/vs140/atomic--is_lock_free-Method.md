---
title: "atomic::is_lock_free Method"
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
ms.assetid: b99d5130-cdda-40a2-b14c-152b13a8ba45
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic::is_lock_free Method
Specifies whether atomic operations on `*this` are *lock free*.  
  
## Syntax  
  
```  
bool is_lock_free() const volatile _NOEXCEPT;  
```  
  
## Return Value  
 `true` if atomic operations on `*this` are lock free; otherwise, `false`.  
  
## Remarks  
 An atomic type is *lock free* if no atomic operations on that type use locks.  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)   
 [atomic Structure](../vs140/atomic-Structure.md)   
 [atomic_is_lock_free](../vs140/atomic_is_lock_free-Function.md)