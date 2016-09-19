---
title: "list::pointer"
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
ms.assetid: d18d9843-2d03-4c8b-91c9-4f8aab8810b1
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::pointer
Provides a pointer to an element in a list.  
  
## Syntax  
  
```unstlib  
  
typedef typename Allocator::pointer pointer;  
  
```  
  
## Remarks  
 A type **pointer** can be used to modify the value of an element.  
  
 In most cases, an [iterator](../vs140/list--iterator.md) should be used to access the elements in a list object.  
  
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)