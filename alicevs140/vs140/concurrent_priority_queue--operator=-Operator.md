---
title: "concurrent_priority_queue::operator= Operator"
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
ms.assetid: ba327251-e095-4aef-a0d5-936c53cd8a53
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_priority_queue::operator= Operator
Assigns the contents of another `concurrent_priority_queue` object to this one. This method is not concurrency-safe.  
  
## Syntax  
  
```  
concurrent_priority_queue& operator=(  
   const concurrent_priority_queue& _Src  
);  
  
concurrent_priority_queue& operator=(  
   concurrent_priority_queue&& _Src  
);  
```  
  
#### Parameters  
 `_Src`  
 The source `concurrent_priority_queue` object.  
  
## Return Value  
 A reference to this `concurrent_priority_queue` object.  
  
## Requirements  
 **Header:** concurrent_priority_queue.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_priority_queue Class](../vs140/concurrent_priority_queue-Class.md)