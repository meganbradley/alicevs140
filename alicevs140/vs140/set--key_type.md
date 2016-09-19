---
title: "set::key_type"
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
ms.assetid: b5325416-ed40-4cb1-a3f0-a4faf4c7845c
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::key_type
A type that describes an object stored as an element of a set in its capacity as sort key.  
  
## Syntax  
  
```  
typedef Key key_type;  
```  
  
## Remarks  
 `key_type` is a synonym for the template parameter `Key`.  
  
 For more information on `Key`, see the Remarks section of the [set Class](../vs140/set-Class.md) topic.  
  
 Note that both `key_type` and [value_type](../vs140/set--value_type.md) are synonyms for the template parameter **Key**. Both types are provided for the set and multiset classes, where they are identical, for compatibility with the map and multimap classes, where they are distinct.  
  
## Example  
 See the example for [value_type](../vs140/set--value_type.md) for an example of how to declare and use `key_type`.  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)