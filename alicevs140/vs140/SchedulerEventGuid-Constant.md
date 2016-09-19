---
title: "SchedulerEventGuid Constant"
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
ms.assetid: 76e2cf6b-e042-4052-8df1-ddfcf453a112
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulerEventGuid Constant
A category GUID describing ETW events fired by the Concurrency Runtime that are directly related to scheduler activity.  
  
## Syntax  
  
```  
const __declspec(selectany) GUID SchedulerEventGuid = { 0xE2091F8A, 0x1E0A, 0x4731, { 0x84, 0xA2, 0x0D, 0xD5, 0x7C, 0x8A, 0x52, 0x61 } };  
```  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [CurrentScheduler Class](../vs140/CurrentScheduler-Class.md)   
 [Scheduler Class](../vs140/Scheduler-Class.md)