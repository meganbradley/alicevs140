---
title: "set::pointer"
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
ms.assetid: 50e8c6f4-a399-4e08-8ff1-4b1f8731f3cd
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::pointer
A type that provides a pointer to an element in a set.  
  
## Syntax  
  
```  
typedef typename allocator_type::pointer pointer;  
```  
  
## Remarks  
 A type **pointer** can be used to modify the value of an element.  
  
 In most cases, an [iterator](../vs140/set--iterator.md) should be used to access the elements in a set object.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)