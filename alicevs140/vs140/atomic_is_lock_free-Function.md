---
title: "atomic_is_lock_free Function"
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
ms.assetid: 6e8cbc6b-bfcf-483b-9e18-c45a03139d2b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic_is_lock_free Function
Specifies whether atomic operations on an `atomic` object are *lock-free*.  
  
## Syntax  
  
```  
template <class T>  
inline bool atomic_is_lock_free(  
   const volatile atomic<T> *Atom  
) _NOEXCEPT;  
template <class T>  
inline bool atomic_is_lock_free(  
   const atomic<T> *Atom  
) _NOEXCEPT;  
```  
  
#### Parameters  
 `Atom`  
 A pointer to an `atomic` object that stores a value of type `T`.  
  
## Return Value  
 `true` if atomic operations on `Atom` are lock-free; otherwise, `false`.  
  
## Remarks  
 An atomic type is lock-free if no atomic operations on that type use locks. If this function returns true, the type is safe to use in signal-handlers.  
  
## Requirements  
 **Header:** atomic  
  
 **Namespace:** std  
  
## See Also  
 [<atomic\>](../vs140/-atomic-.md)   
 [atomic Structure](../vs140/atomic-Structure.md)