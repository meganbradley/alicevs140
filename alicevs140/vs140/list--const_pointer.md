---
title: "list::const_pointer"
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
ms.assetid: e3bea75d-ca75-476f-83e4-a91b17785fd5
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::const_pointer
Provides a pointer to a `const` element in a list.  
  
## Syntax  
  
```unstlib  
  
typedef typename Allocator::const  
_  
pointer const  
_  
pointer;  
  
```  
  
## Remarks  
 A type `const_pointer` cannot be used to modify the value of an element.  
  
 In most cases, an [iterator](../vs140/list--iterator.md) should be used to access the elements in a list object.  
  
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)