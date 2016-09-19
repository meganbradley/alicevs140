---
title: "IScheduler::GetId Method"
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
ms.assetid: 3280bda0-b1a4-4c8f-89e1-8869a0c9ee9d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IScheduler::GetId Method
Returns a unique identifier for the scheduler.  
  
## Syntax  
  
```  
virtual unsigned int GetId() const =0;  
```  
  
## Return Value  
 A unique integer identifier.  
  
## Remarks  
 You should use the [GetSchedulerId](../vs140/GetSchedulerId-Function.md) function to obtain a unique identifier for the object that implements the `IScheduler` interface, before you use the interface as a parameter to methods supplied by the Resource Manager. You are expected to return the same identifier when the `GetId` function is invoked.  
  
 An identifier obtained from a different source could result in undefined behavior.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IScheduler Structure](../vs140/IScheduler-Structure.md)