---
title: "concurrent_priority_queue::try_pop Method"
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
ms.assetid: 91819a8b-d751-4196-a5d4-b85454575b7b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_priority_queue::try_pop Method
Removes and returns the highest priority element from the queue if the queue is non-empty. This method is concurrency-safe.  
  
## Syntax  
  
```  
bool try_pop(  
   reference _Elem  
);  
```  
  
#### Parameters  
 `_Elem`  
 A reference to a variable that will be populated with the highest priority element, if the queue is non-empty.  
  
## Return Value  
 `true` if a value was popped, `false` otherwise.  
  
## Requirements  
 **Header:** concurrent_priority_queue.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_priority_queue Class](../vs140/concurrent_priority_queue-Class.md)