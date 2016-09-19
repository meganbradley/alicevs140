---
title: "invalid_compute_domain Class"
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
ms.assetid: ac7a7166-8bdb-4db1-8caf-ea129ab5117e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_compute_domain Class
The exception that's thrown when the runtime can't start a kernel by using the compute domain specified at the [parallel_for_each](../vs140/parallel_for_each-Function--C---AMP-.md) call site.  
  
## Syntax  
  
```  
class invalid_compute_domain : public runtime_exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[invalid_compute_domain::invalid_compute_domain Constructor](../vs140/invalid_compute_domain--invalid_compute_domain-Constructor.md)|Initializes a new instance of the `invalid_compute_domain` class.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `runtime_exception`  
  
 `invalid_compute_domain`  
  
## Requirements  
 **Header:** amprt.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [Concurrency Namespace (C++ Accelerated Massive Parallelism)](../vs140/Concurrency-Namespace--C---AMP-.md)