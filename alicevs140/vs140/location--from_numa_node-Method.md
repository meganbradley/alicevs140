---
title: "location::from_numa_node Method"
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
ms.assetid: 9d7ed000-fc47-44d0-9d53-246f17f1a08c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# location::from_numa_node Method
Returns a `location` object which represents a given NUMA node.  
  
## Syntax  
  
```  
static location __cdecl from_numa_node(  
   unsigned short _NumaNodeNumber  
);  
```  
  
#### Parameters  
 `_NumaNodeNumber`  
 The NUMA node number to construct a location for.  
  
## Return Value  
 A location representing the NUMA node specified by the `_NumaNodeNumber` parameter.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [location Class](../vs140/location-Class.md)