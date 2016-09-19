---
title: "Command-Line Profiling of Stand-Alone Applications"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a47f2bf2-186d-4120-bb79-34e2f3a1ee42
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command-Line Profiling of Stand-Alone Applications
This section describes the procedures and options for collecting performance data for stand-alone (client) applications by using the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools from the command line.  
  
## Common Tasks  
  
|Task|Related content|  
|----------|---------------------|  
|**Collect application statistics:** Use the sampling method to collect performance statistics. Sampling data is useful for analyzing CPU utilization issues and for understanding the general performance characteristics of an application.|-   [Collecting Application Statistics for Stand-Alone Applications by Using the Profiler Command-Line](../vs140/Collecting-Application-Statistics-for-Stand-Alone-Applications-by-Using-the-Profiler-Command-Line.md)|  
|**Collect detailed timing data:** Use the instrumentation method to collect detailed timing information. Instrumentation data is useful for analyzing I/O issues and for fine-grained analysis of application scenarios.|-   [Collecting Detailed Timing Data for a Stand-Alone Application by Using the Profiler Command-Line](../vs140/Collecting-Detailed-Timing-Data-for-a-Stand-Alone-Application-by-Using-the-Profiler-Command-Line.md)|  
|**Collect .NET memory data:** Use sampling or instrumentation to collect .NET memory allocation data that shows you the size and number of allocated objects. You can also collect object lifetime data that shows you the size and number of objects that are reclaimed in each garbage collection generation.|-   [Collecting .NET Memory Data for Stand-Alone Applications Using the Profiler Command-Line](../vs140/Collecting-.NET-Framework-Memory-Data-for-Stand-Alone-Applications-by-Using-the-Profiler-Command-Line.md)|  
|**Collect concurrency data:** Use the concurrency method to collect resource contention data and thread activity data that shows you CPU utilization, thread contention, thread migration, synchronization delays, areas of overlapped I/O, and other system events.|-   [Collecting Concurrency Data for Stand-Alone Applications by Using the Profiler Command Line](../vs140/Collecting-Concurrency-Data-for-Stand-Alone-Applications-by-Using-the-Profiler-Command-Line.md)|  
|**Add tier-interaction data:** You can add performance data about synchronous ADO.NET calls that the application made to a Microsoft [!INCLUDE[ssNoVersion](../vs140/includes/ssNoVersion_md.md)] database. Adding tier interaction data to a profiling run requires specific procedures with the command line profiling tools.|-   [Adding Tier Interaction Data to Profiling Data From the Command Line](../vs140/Adding-tier-interaction-data-from-the-command-line.md)|  
|**Try it out:** Use step-by-step procedures to profile a sample client application by using the sampling or instrumentation method.|-   [Walkthrough: Command-Line Profiling Using Sampling](../vs140/Walkthrough--Command-Line-Profiling-Using-Sampling.md)<br />-   [Walkthrough: Command-Line Profiling Using Instrumentation](../vs140/Walkthrough--Command-Line-Profiling-Using-Instrumentation.md)|  
  
## Related Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile ASP.NET applications**|-   [Command-Line Profiling of ASP.NET Web Applications](../vs140/Command-Line-Profiling-of-ASP.NET-Web-Applications.md)|  
|**Profile services**|-   [Command-Line Profiling of Services](../vs140/Command-Line-Profiling-of-Services.md)|