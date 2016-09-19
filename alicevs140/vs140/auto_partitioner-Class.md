---
title: "auto_partitioner Class"
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
ms.assetid: 7cc08e5d-20b4-47a4-b4b5-c214a78f5a9e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# auto_partitioner Class
The             `auto_partitioner` class represents the default method             `parallel_for`,             `parallel_for_each` and             `parallel_transform` use to partition the range they iterates over. This method of partitioning employes range stealing for load balancing as well as per-iterate cancellation.  
  
## Syntax  
  
```  
class auto_partitioner;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[auto_partitioner::auto_partitioner Constructor](#auto_partitioner__auto_partitioner_constructor)|Constructs a                                         `auto_partitioner` object.|  
|[auto_partitioner::~auto_partitioner Destructor](#auto_partitioner___dtorauto_partitioner_destructor)|Destroys a                                         `auto_partitioner` object.|  
  
## Inheritance Hierarchy  
 `auto_partitioner`  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
##  <a name="auto_partitioner___dtorauto_partitioner_destructor"></a>  auto_partitioner::~auto_partitioner Destructor  
 Destroys a                 `auto_partitioner` object.  
  
```  
~auto_partitioner();  
```  
  
##  <a name="auto_partitioner__auto_partitioner_constructor"></a>  auto_partitioner::auto_partitioner Constructor  
 Constructs a                 `auto_partitioner` object.  
  
```  
auto_partitioner();  
```  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)