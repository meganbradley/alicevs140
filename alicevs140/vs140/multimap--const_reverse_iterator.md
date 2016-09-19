---
title: "multimap::const_reverse_iterator"
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
ms.assetid: 3f859301-63e4-42d3-b0dc-ad0d8851e234
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multimap::const_reverse_iterator
A type that provides a bidirectional iterator that can read any **const** element in the multimap.  
  
## Syntax  
  
```  
typedef std::reverse_iterator<const_iterator> const_reverse_iterator;  
```  
  
## Remarks  
 A type `const_reverse_iterator` cannot modify the value of an element and is use to iterate through the multimap in reverse.  
  
 The `const_reverse_iterator` defined by multimap points to objects of [value_type](../vs140/multimap--value_type.md), which are of type `pair`*<***const Key**, **Type***>*. The value of the key is available through the first member pair and the value of the mapped element is available through the second member of the pair.  
  
 To dereference a `const_reverse_iterator` `crIter` pointing to an element in a multimap, use the **->** operator.  
  
 To access the value of the key for the element, use `crIter` -> **first**, which is equivalent to (\*`crIter`).**first**. To access the value of the mapped datum for the element, use `crIter` -> **second**, which is equivalent to (\*`crIter`).**first**.  
  
## Example  
 See the example for [rend](../vs140/multimap--rend.md) for an example of how to declare and use `const_reverse_iterator`.  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [multimap Class](../vs140/multimap-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)