---
title: "multiset::pointer"
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
ms.assetid: 5097d56b-b9f3-48b8-9579-1aecb82b359e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::pointer
A type that provides a pointer to an element in a multiset.  
  
## Syntax  
  
```  
typedef typename allocator_type::pointer pointer;  
```  
  
## Remarks  
 A type **pointer** can be used to modify the value of an element.  
  
 In most cases, an [iterator](../vs140/multiset--iterator.md) should be used to access the elements in a multiset object.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [multiset Class](../vs140/multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)