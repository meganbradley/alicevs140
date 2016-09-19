---
title: "concurrent_priority_queue::push Method"
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
ms.assetid: 4376ec50-7e27-46b9-b254-c286d09a0a85
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_priority_queue::push Method
Adds an element to the concurrent priority queue. This method is concurrency-safe.  
  
## Syntax  
  
```  
void push(  
   const value_type& _Elem  
);  
  
void push(  
   value_type&& _Elem  
);  
```  
  
#### Parameters  
 `_Elem`  
 The element to be added to the concurrent priority queue.  
  
## Requirements  
 **Header:** concurrent_priority_queue.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_priority_queue Class](../vs140/concurrent_priority_queue-Class.md)