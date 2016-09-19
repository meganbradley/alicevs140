---
title: "concurrent_queue::unsafe_begin Method"
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
ms.assetid: 91524d7e-689c-4837-b8d8-00c00e6d7816
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_queue::unsafe_begin Method
Returns an iterator of type `iterator` or `const_iterator` to the beginning of the concurrent queue. This method is not concurrency-safe.  
  
## Syntax  
  
```  
iterator unsafe_begin();  
  
const_iterator unsafe_begin() const;  
```  
  
## Return Value  
 An iterator of type `iterator` or `const_iterator` to the beginning of the concurrent queue object.  
  
## Remarks  
 The iterators for the `concurrent_queue` class are primarily intended for debugging, as they are slow, and iteration is not concurrency-safe with respect to other queue operations.  
  
## Requirements  
 **Header:** concurrent_queue.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_queue Class](../vs140/concurrent_queue-Class.md)