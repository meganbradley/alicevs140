---
title: "concurrent_priority_queue::swap Method"
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
ms.assetid: b5229ecf-8d75-41b8-955d-e1eb6a93b397
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_priority_queue::swap Method
Swaps the contents of two concurrent priority queues. This method is not concurrency-safe.  
  
## Syntax  
  
```  
void swap(  
   concurrent_priority_queue& _Queue  
);  
```  
  
#### Parameters  
 `_Queue`  
 The `concurrent_priority_queue` object to swap contents with.  
  
## Requirements  
 **Header:** concurrent_priority_queue.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_priority_queue Class](../vs140/concurrent_priority_queue-Class.md)