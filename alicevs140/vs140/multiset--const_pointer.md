---
title: "multiset::const_pointer"
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
ms.assetid: eecb5e0d-aaf1-4cc6-8b12-c6902e8916a3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::const_pointer
A type that provides a pointer to a **const** element in a multiset.  
  
## Syntax  
  
```  
typedef typename allocator_type::const_pointer const_pointer;  
```  
  
## Remarks  
 A type `const_pointer` cannot be used to modify the value of an element.  
  
 In most cases, an [iterator](../vs140/multiset--iterator.md) should be used to access the elements in a multiset object.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [multiset Class](../vs140/multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)