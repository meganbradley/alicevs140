---
title: "DA0501: Average CPU consumption by the Process being profiled."
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b01946b4-75e3-47d5-a1a1-cebfae66a3af
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DA0501: Average CPU consumption by the Process being profiled.
|||  
|-|-|  
|Rule Id|DA501|  
|Category|Resource Monitoring|  
|Profiling method|All|  
|Message|Average CPU consumption by the Process being profiled.|  
|Rule type|Information|  
  
 When you profile by using the sampling, .NET memory, or resource contention methods, you must collect at least 10 samples to trigger this rule.  
  
## Rule Description  
 This message reports the percentage of time that a processor was busy executing instructions from the application. The reported value is the average over all the measurement intervals in which the process being profiled was active. The value of value can be greater than 100% on a machine with more than one processor.  
  
## How to Use Rule Data  
 Use the rule value to compare the performance of different versions or builds of the program or to understand the performance of the application under different test scenarios.