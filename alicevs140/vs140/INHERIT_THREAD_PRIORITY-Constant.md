---
title: "INHERIT_THREAD_PRIORITY Constant"
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
ms.assetid: e641b23b-63a8-48c6-b63a-3440cf973fa6
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# INHERIT_THREAD_PRIORITY Constant
Special value for the policy key `ContextPriority` indicating that the thread priority of all contexts in the scheduler should be the same as that of the thread which created the scheduler.  
  
## Syntax  
  
```  
const unsigned int INHERIT_THREAD_PRIORITY = 0x0000F000;  
```  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)