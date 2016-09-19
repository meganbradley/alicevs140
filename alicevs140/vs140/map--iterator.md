---
title: "map::iterator"
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
ms.assetid: 0ea2460f-f8b2-44bb-bc3f-434a53962d7a
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# map::iterator
A type that provides a bidirectional iterator that can read or modify any element in a map.  
  
## Syntax  
  
```  
typedef implementation-defined iterator;  
```  
  
## Remarks  
 The **iterator** defined by map points to elements that are objects of [value_type](../vs140/map--value_type.md), that is of type `pair`*<***const Key**, **Type***>*, whose first member is the key to the element and whose second member is the mapped datum held by the element.  
  
 To dereference an **iterator** `Iter` pointing to an element in a map, use the **->** operator.  
  
 To access the value of the key for the element, use `Iter` -> **first**, which is equivalent to (\*`Iter`).**first**. To access the value of the mapped datum for the element, use `Iter` -> **second**, which is equivalent to (\*`Iter`).**second**.  
  
## Example  
 See example for [begin](../vs140/map--begin.md) for an example of how to declare and use **iterator**.  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [map Class](../vs140/map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)