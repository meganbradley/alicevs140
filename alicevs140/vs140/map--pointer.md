---
title: "map::pointer"
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
ms.assetid: 92b2ea9e-05f5-43a9-a0e7-4f8af73e3944
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# map::pointer
A type that provides a pointer to an element in a map.  
  
## Syntax  
  
```  
typedef typename allocator_type::pointer pointer;  
```  
  
## Remarks  
 A type **pointer** can be used to modify the value of an element.  
  
 In most cases, an [iterator](../vs140/map--iterator.md) should be used to access the elements in a map object.  
  
## Requirements  
 **Header:** <map\>  
  
 **Namespace:** std  
  
## See Also  
 [map Class](../vs140/map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)