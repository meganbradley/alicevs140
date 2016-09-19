---
title: "vector::const_reverse_iterator"
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
ms.assetid: 148d93b0-e228-41bc-b4e9-b9378936aabc
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vector::const_reverse_iterator
A type that provides a random-access iterator that can read any **const** element in the vector.  
  
## Syntax  
  
```  
typedef std::reverse_iterator<const_iterator> const_reverse_iterator;  
```  
  
## Remarks  
 A type `const_reverse_iterator` cannot modify the value of an element and is used to iterate through the vector in reverse.  
  
## Example  
 See [rbegin](../vs140/vector--rbegin.md) for an example of how to declare and use an iterator.  
  
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)