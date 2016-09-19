---
title: "thread::join Method"
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
ms.assetid: 6e45b2d2-15a6-4221-a825-105a14431115
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# thread::join Method
Blocks until the thread of execution that's associated with the calling object completes.  
  
## Syntax  
  
```  
void join();  
```  
  
## Remarks  
 If the call succeeds, subsequent calls to [get_id](../vs140/thread--get_id-Method.md) for the calling object return a default [thread::id](../vs140/thread--id-Class.md) that does not compare equal to the `thread::id` of any existing thread; if the call does not succeed, the value that's returned by `get_id` is unchanged.  
  
## Requirements  
 **Header:** thread  
  
 **Namespace:** std  
  
## See Also  
 [thread Class](../vs140/thread-Class.md)   
 [<thread\>](../vs140/-thread-.md)