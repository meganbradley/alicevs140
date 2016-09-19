---
title: "list::const_reverse_iterator"
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
ms.assetid: 6ed5190a-b1d5-4507-8d5d-36d41a8078ef
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# list::const_reverse_iterator
A type that provides a bidirectional iterator that can read any **const** element in a list.  
  
## Syntax  
  
```  
typedef std::reverse_iterator<const_iterator> const_reverse_iterator;  
```  
  
## Remarks  
 A type `const_reverse_iterator` cannot modify the value of an element and is used to iterate through the list in reverse.  
  
## Example  
 See the example for [rbegin](../vs140/list--rbegin.md).  
  
## Requirements  
 **Header:** <list\>  
  
 **Namespace:** std  
  
## See Also  
 [list Class](../vs140/list-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)