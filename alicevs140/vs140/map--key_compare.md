---
title: "map::key_compare"
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
ms.assetid: 60ed36d7-2f73-419a-bf12-67a7f97192f0
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# map::key_compare
A type that provides a function object that can compare two sort keys to determine the relative order of two elements in the map.  
  
## Syntax  
  
```  
typedef Traits key_compare;  
```  
  
## Remarks  
 `key_compare` is a synonym for the template parameter `Traits`.  
  
 For more information on `Traits` see the [map Class](../vs140/map-Class.md) topic.  
  
## Example  
 See example for [key_comp](../vs140/map--key_comp.md) for an example of how to declare and use `key_compare`.  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [map Class](../vs140/map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)