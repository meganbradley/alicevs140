---
title: "multimap::key_compare"
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
ms.assetid: 91a516f6-24f3-442d-8264-fcb2638682ee
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multimap::key_compare
A type that provides a function object that can compare two sort keys to determine the relative order of two elements in the multimap.  
  
## Syntax  
  
```  
typedef Traits key_compare;  
```  
  
## Remarks  
 **key_compare** is a synonym for the template parameter `Traits`.  
  
 For more information on `Traits` see the [multimap Class](../vs140/multimap-Class.md) topic.  
  
## Example  
 See the example for [key_comp](../vs140/multimap--key_comp.md) for an example of how to declare and use `key_compare`.  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [multimap Class](../vs140/multimap-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)