---
title: "multiset::key_compare"
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
ms.assetid: 012ee40a-b0e8-446f-8e75-8504dc50a079
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multiset::key_compare
A type that provides a function object that can compare two sort keys to determine the relative order of two elements in the multiset.  
  
## Syntax  
  
```  
typedef Compare key_compare;  
```  
  
## Remarks  
 **key_compare** is a synonym for the template parameter `Compare`.  
  
 For more information on `Compare`, see the Remarks section of the [multiset Class](../vs140/multiset-Class.md) topic.  
  
## Example  
 See the example for [key_comp](../vs140/multiset--key_comp.md) for an example of how to declare and use `key_compare`.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [multiset Class](../vs140/multiset-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)