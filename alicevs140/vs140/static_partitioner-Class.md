---
title: "static_partitioner Class"
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
ms.assetid: 2b3dbdf0-6eb9-49f6-8639-03df1d974143
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# static_partitioner Class
The             `static_partitioner` class represents a static partitioning of the range iterated over by             `parallel_for`. The partitioner divides the range into as many chunks as there are workers available to the underyling scheduler.  
  
## Syntax  
  
```  
class static_partitioner;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[static_partitioner::static_partitioner Constructor](#static_partitioner__static_partitioner_constructor)|Constructs a                                         `static_partitioner` object.|  
|[static_partitioner::~static_partitioner Destructor](#static_partitioner___dtorstatic_partitioner_destructor)|Destroys a                                         `static_partitioner` object.|  
  
## Inheritance Hierarchy  
 `static_partitioner`  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
##  <a name="static_partitioner___dtorstatic_partitioner_destructor"></a>  static_partitioner::~static_partitioner Destructor  
 Destroys a                 `static_partitioner` object.  
  
```  
~static_partitioner();  
```  
  
##  <a name="static_partitioner__static_partitioner_constructor"></a>  static_partitioner::static_partitioner Constructor  
 Constructs a                 `static_partitioner` object.  
  
```  
static_partitioner();  
```  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)