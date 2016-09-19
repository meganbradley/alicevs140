---
title: "allocator_traits::construct Method"
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
ms.assetid: 3b19ee5c-8e68-4ddb-97d7-51184c715987
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# allocator_traits::construct Method
Static method that uses a specified allocator to construct an object.  
  
## Syntax  
  
```cpp  
template<class Uty, class Types>  
    static void construct(Alloc& al, Uty *ptr, Types&&... args);  
```  
  
#### Parameters  
 `al`  
 An allocator object.  
  
 `ptr`  
 A pointer to the location where the object is to be constructed.  
  
 `args`  
 A list of arguments that is passed to the object constructor.  
  
## Remarks  
 The static member function calls `al.construct(ptr, args...)`, if that expression is well formed; otherwise it evaluates `::new (static_cast<void *>(ptr)) Uty(std::forward<Types>(args)...)`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [allocator::construct](../vs140/allocator--construct.md)   
 [allocator_traits Class](../vs140/allocator_traits-Class.md)