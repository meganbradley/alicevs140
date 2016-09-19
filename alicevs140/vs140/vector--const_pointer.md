---
title: "vector::const_pointer"
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
ms.assetid: a747fadc-0ea8-4468-999e-e75b56edbe37
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::const_pointer
A type that provides a pointer to a **const** element in a vector.  
  
## Syntax  
  
```  
  
typedef typename Allocator::const_pointer const_pointer;  
  
```  
  
## Remarks  
 A type `const_pointer` cannot be used to modify the value of an element.  
  
 An [iterator](../vs140/vector--iterator.md) is more commonly used to access a vector element.  
  
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)