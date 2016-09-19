---
title: "concurrent_priority_queue::size Method"
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
ms.assetid: fa6dee23-2e1c-4365-a246-cf8bb3cee817
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_priority_queue::size Method
Returns the number of elements in the concurrent priority queue. This method is concurrency-safe.  
  
## Syntax  
  
```  
size_type size() const;  
```  
  
## Return Value  
 The number of elements in this `concurrent_priority_queue` object.  
  
## Remarks  
 The returned size is guaranteed to include all elements added by calls to the function `push`. However, it may not reflect results of pending concurrent operations.  
  
## Requirements  
 **Header:** concurrent_priority_queue.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_priority_queue Class](../vs140/concurrent_priority_queue-Class.md)