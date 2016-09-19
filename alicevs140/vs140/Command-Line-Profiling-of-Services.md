---
title: "Command-Line Profiling of Services"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f0d62318-b0e8-49c6-9a30-9f7a6adef2f6
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command-Line Profiling of Services
This section describes the procedures and options for collecting performance data for Windows services by using [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools from the command line.  
  
> [!NOTE]
>  Enhanced security features in Windows 8 and Windows Server 2012 required significant changes in the way the Visual Studio profiler collects data on these platforms. Windows Store apps also require new collection techniques. See [Profiling Windows 8 and Windows Server 2012 applications](../vs140/Performance-Tools-on-Windows-8-and-Windows-Server-2012-applications.md).  
  
## Common Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Collect application statistics:** Use the sampling method to collect performance statistics. Sampling data is useful for analyzing CPU utilization issues and for understanding the general performance characteristics of an application.|-   [Collecting Application Statistics for Services Using the Profiler Sampling Method](../vs140/Collecting-Application-Statistics-for-Services-by-Using-the-Profiler-Sampling-Method.md)|  
|**Collect detailed timing data:** Use the instrumentation method to collect detailed timing information. Instrumentation data is useful for analyzing IO issues and for fine-grained analysis of application scenarios.|-   [Collecting Detailed Timing Data for Services Using the Instrumentation Method from the Profiler Command Line](../vs140/Collecting-Detailed-Timing-Data-for-Services-by-Using-the-Instrumentation-Method-from-the-Profiler-Command-Line.md)|  
|**Collect .NET memory data:** Use sampling or instrumentation to collect .NET memory allocation data that shows you the size and number of allocated objects. You can also collect object lifetime data that shows you the size and number of objects that are reclaimed in each garbage collection generation.|-   [Collecting .NET Memory Data from Services using the Profiler Command Line](../vs140/Collecting-Memory-Data-from-.NET-Framework-Services-by-Using-the-Profiler-Command-Line.md)|  
|**Collect concurrency data:** Use the concurrency method to collect resource contention data and thread activity data that shows you CPU utilization, thread contention, thread migration, synchronization delays, areas of overlapped IO, and other system events.|-   [Collecting Concurrency Data for Services by Using the Profiler Command Line](../vs140/Collecting-Concurrency-Data-for-a-Service-by-Using-the-Profiler-Command-Line.md)|  
|**Add tier interaction data:** You can add performance data about synchronous ADO.NET calls that the service made to a Microsoft [!INCLUDE[ssNoVersion](../vs140/includes/ssNoVersion_md.md)] database.|-   [How to: Add Tier Interaction Data to Profiling Data From the Command Line](../vs140/Adding-tier-interaction-data-from-the-command-line.md)|  
  
## Related Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile stand-alone (client) applications**|-   [Command-Line Profiling of Stand-Alone Applications](../vs140/Command-Line-Profiling-of-Stand-Alone-Applications.md)|  
|**Profile ASP.NET applications**|-   [Command-Line Profiling of ASP.NET Applications](../vs140/Command-Line-Profiling-of-ASP.NET-Web-Applications.md)|