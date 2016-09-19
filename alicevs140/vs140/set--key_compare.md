---
title: "set::key_compare"
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
ms.assetid: 7d1ee2b6-aeae-491f-829a-204709ef655d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::key_compare
A type that provides a function object that can compare two sort keys to determine the relative order of two elements in the set.  
  
## Syntax  
  
```  
typedef Traits key_compare;  
```  
  
## Remarks  
 `key_compare` is a synonym for the template parameter `Traits`.  
  
 For more information on `Traits` see the [set Class](../vs140/set-Class.md) topic.  
  
 Note that both `key_compare` and [value_compare](../vs140/set--value_compare.md) are synonyms for the template parameter **Traits**. Both types are provided for the set and multiset classes, where they are identical, for compatibility with the map and multimap classes, where they are distinct.  
  
## Example  
 See the example for [key_comp](../vs140/set--key_comp.md) for an example of how to declare and use `key_compare`.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)