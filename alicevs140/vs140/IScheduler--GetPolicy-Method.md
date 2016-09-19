---
title: "IScheduler::GetPolicy Method"
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
ms.assetid: 0465ee03-9c15-477a-9106-6cae47acf75c
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IScheduler::GetPolicy Method
Returns a copy of the scheduler's policy. For more information on scheduler policies, see [SchedulerPolicy](../vs140/SchedulerPolicy-Class.md).  
  
## Syntax  
  
```  
virtual SchedulerPolicy GetPolicy() const =0;  
```  
  
## Return Value  
 A copy of the scheduler's policy.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IScheduler Structure](../vs140/IScheduler-Structure.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)