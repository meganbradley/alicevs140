---
title: "Scheduler::Scheduler Constructor"
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
ms.assetid: b7c4e760-02ae-414e-b6db-1e6a6ddb671b
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scheduler::Scheduler Constructor
An object of the `Scheduler` class can only created using factory methods, or implicitly.  
  
## Syntax  
  
```  
Scheduler();  
```  
  
## Remarks  
 The process' default scheduler is created implicitly when you utilize many of the runtime functions which require a scheduler to be attached to the calling context. Methods within the `CurrentScheduler` class and features of the PPL and agents layers typically perform implicit attachment.  
  
 You can also create a scheduler explicitly through either the `CurrentScheduler::Create` method or the `Scheduler::Create` method.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [CurrentScheduler Class](../vs140/CurrentScheduler-Class.md)   
 [CurrentScheduler::Create Method](../vs140/CurrentScheduler--Create-Method.md)   
 [Scheduler::Create Method](../vs140/Scheduler--Create-Method.md)