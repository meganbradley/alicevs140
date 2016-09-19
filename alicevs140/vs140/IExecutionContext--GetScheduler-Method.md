---
title: "IExecutionContext::GetScheduler Method"
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
ms.assetid: d27e8334-da6d-471b-8f3b-9802fa04e0b3
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IExecutionContext::GetScheduler Method
Returns an interface to the scheduler this execution context belongs to.  
  
## Syntax  
  
```  
virtual IScheduler * GetScheduler() =0;  
```  
  
## Return Value  
 An `IScheduler` interface.  
  
## Remarks  
 You are required to initialize the execution context with a valid `IScheduler` interface before you use it as a parameter to methods supplied by the Resource Manager.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IExecutionContext Structure](../vs140/IExecutionContext-Structure.md)