---
title: "multimap::pointer"
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
ms.assetid: c9a097c4-5be2-4d5f-9285-7b9435a1a932
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multimap::pointer
A type that provides a pointer to an element in a multimap.  
  
## Syntax  
  
```  
typedef typename allocator_type::pointer pointer;  
```  
  
## Remarks  
 A type **pointer** can be used to modify the value of an element.  
  
 In most cases, an [iterator](../vs140/multimap--iterator.md) should be used to access the elements in a multimap object.  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [multimap Class](../vs140/multimap-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)