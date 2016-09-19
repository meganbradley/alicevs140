---
title: "concurrent_queue::push Method"
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
ms.assetid: a0013721-3a3b-4307-a29e-710d8c39d8a9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_queue::push Method
Enqueues an item at tail end of the concurrent queue. This method is concurrency-safe.  
  
## Syntax  
  
```  
void push(  
   const _Ty& _Src  
);  
  
void push(  
   _Ty&& _Src  
);  
```  
  
#### Parameters  
 `_Src`  
 The item to be added to the queue.  
  
## Remarks  
 `push` is concurrency-safe with respect to calls to the methods `push`, `try_pop`, and `empty`.  
  
## Requirements  
 **Header:** concurrent_queue.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_queue Class](../vs140/concurrent_queue-Class.md)