---
title: "set::const_pointer"
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
ms.assetid: 1bbac8ab-e61a-41c5-acd8-72a36467f48a
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::const_pointer
A type that provides a pointer to a **const** element in a set.  
  
## Syntax  
  
```  
typedef typename allocator_type::const_pointer const_pointer;  
```  
  
## Remarks  
 A type `const_pointer` cannot be used to modify the value of an element.  
  
 In most cases, a [const_iterator](../vs140/set--const_iterator.md) should be used to access the elements in a const set object.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)