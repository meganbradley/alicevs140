---
title: "deque::const_pointer"
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
ms.assetid: a62daa94-4dd9-42e3-8fc1-845ea036cf8e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::const_pointer
Provides a pointer to a `const` element in a deque.  
  
## Syntax  
  
```unstlib  
  
typedef typename Allocator::const_pointer const_pointer;  
  
```  
  
## Remarks  
 A type `const_pointer` cannot be used to modify the value of an element. An [iterator](../vs140/deque--iterator.md) is more commonly used to access a deque element.  
  
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)