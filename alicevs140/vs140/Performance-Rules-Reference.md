---
title: "Performance Rules Reference"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 59fc9424-76ca-4365-ae47-bb14a736c9c2
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Performance Rules Reference
The performance rules of the Profiling Tools provide additional warnings and information about the performance of your application. Performance rules analyze data in a profiling run that is collected from sources such as Windows and processor performance counters. Rule messages appear in the Error Output window of the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] integrated development environment. Messages are listed with one of the following rule levels:  
  
|||  
|-|-|  
|**Error**|Few rules generate Error messages because most performance problems are not outright errors. An Error message can indicate a failure to collect profiling data.|  
|**Warning**|Warnings indicate an area of your application that can potentially be a source of performance problems or that might benefit from optimizations.|  
|**Information**|Information messages indicate that either the analysis of a rule condition did not reach the threshold to generate an Error message, or that the information in the message is useful but does not reflect a performance problem.|  
  
## In This Section  
 [Performance Rules by ID](../Topic/Performance%20Rules%20by%20ID.md)  
  
 The Profiling Tools performance rules are organized in four categories:  
  
|||  
|-|-|  
|[.NET Framework Usage Performance Rules](../Topic/.NET%20Framework%20Usage%20Performance%20Rules.md)|Rules that help you use the .NET Framework efficiently.|  
|[Memory and Paging Performance Rules](../vs140/Memory-and-Paging-Performance-Rules.md)|Rules that analyze the managed memory and paging behavior of your application.|  
|[Profiling Tools Usage Rules](../Topic/Profiling%20Tools%20Usage%20Rules.md)|Rules that help you use the Profiling Tools efficiently.|  
|[Resource Monitoring Performance Rules](../vs140/Resource-Monitoring-Performance-Rules.md)|Information messages about processor and memory utilization in a profiling run.|