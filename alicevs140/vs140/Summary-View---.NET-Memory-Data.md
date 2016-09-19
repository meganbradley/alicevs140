---
title: "Summary View - .NET Memory Data"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0cb317c3-0ae6-4531-aaa8-447576eec037
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Summary View - .NET Memory Data
The Summary view displays information about the .NET functions and types that allocated the most memory, and the types that were created the most times in a profiling run. For more information, including a description of the Notification Links and Report lists, see [Summary View](../vs140/Summary-View.md).  
  
## Timeline Graph  
 The timeline graph in the Summary view shows the processor (CPU) utilization by the profiled application over the time that the profiling occurred. You can use the timeline graph to filter the view to a selected time span. For more information, see [How to: Filter Profiling Reports from the Summary Timeline](../vs140/How-to--Filter-Report-Views-from-the-Summary-Timeline.md).  
  
## Functions Allocating Most Memory  
 Lists the functions that allocated the greatest number of bytes of memory in the profiling run.  
  
|Column|Description|  
|------------|-----------------|  
|**Name**|The name of the function.|  
|**Bytes %**|The percentage of all allocated bytes in the profiling run that were allocated by this function or by a child function that was called by this function.|  
  
## Types with Most Memory Allocated  
 Lists the types for which the greatest number of bytes of memory were allocated in the profiling run.  
  
|Column|Description|  
|------------|-----------------|  
|**Name**|The name of the type.|  
|**Bytes %**|The percentage of all allocated bytes in the profiling run that were allocated for this type.|  
  
## Types with Most Instances  
 Lists the types that were created the most times during the profiling run. had  
  
|Column|Description|  
|------------|-----------------|  
|**Name**|The name of the type.|  
|**Instances %**|The percentage of the total number of.NET objects that were created in the profiling run that were instances of this type.|  
  
## See Also  
 [Summary View - Profiler Sampling Data](../vs140/Summary-View---Sampling-Data.md)   
 [Summary View - Profiler Instrumentation Data](../vs140/Summary-View---Instrumentation-Data.md)