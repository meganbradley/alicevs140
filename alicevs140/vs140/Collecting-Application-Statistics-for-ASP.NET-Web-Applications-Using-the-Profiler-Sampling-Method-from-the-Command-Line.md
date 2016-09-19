---
title: "Collecting Application Statistics for ASP.NET Web Applications Using the Profiler Sampling Method from the Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f8383ab1-eb49-4d3f-8608-d8b4d51a81be
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collecting Application Statistics for ASP.NET Web Applications Using the Profiler Sampling Method from the Command Line
This section describes the procedures and options for collecting performance statistics for an ASP.NET Web application by using the **VSPerfASPNETCmd** and **VSPerfCmd** command-line tool and the sampling profiling method.  
  
> [!NOTE]
>  Enhanced security features in Windows 8 and Windows Server 2012 required significant changes in the way the Visual Studio profiler collects data on these platforms. Windows Store apps also require new collection techniques. See [Profiling Windows 8 and Windows Server 2012 applications](../vs140/Performance-Tools-on-Windows-8-and-Windows-Server-2012-applications.md).  
  
> [!NOTE]
>  Although the **VSPerfCmd** tool gives you complete access to Profiling Tools functionality, including pausing and resuming profiling, and collecting additional data from processor and Windows performance counters, you should use use the  **VSPerfASPNETCmd** command line tool when you do not need this functionality. The **VSPerfASPNETCmd** command line tool is the preferred method when your are profiling ASP.NET Web sites using the stand-alone profiler. Compared with the [VSPerfCmd](../vs140/VSPerfCmd.md) command line tool, no environment variables need to be set, and rebooting the computer is not required. For more information, see [Rapid Web Site Profiling with VSPerfASPNETCmd](../vs140/Rapid-Web-Site-Profiling-with-VSPerfASPNETCmd.md).  
  
## Common Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Attach the profiler to an ASP.NET application**|-   [How to: Attach the Profiler to an ASP.NET Web Application to Collect Application Statistics Using the Command Line](../vs140/How-to--Attach-the-Profiler-to-an-ASP.NET-Web-Application-to-Collect-Application-Statistics-by-Using-the-Command-Line.md)|  
  
## Related Tasks  
  
### Profiling ASP.NET Web Applications  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile by using the instrumentation method**|-   [Collecting Detailed Timing Data for an ASP.NET Web Application Using the Profiler Instrumentation Method from the Command Line](../vs140/Collecting-Detailed-Timing-Data-for-an-ASP.NET-Web-Application-Using-the-Profiler-Instrumentation-Method-from-the-Command-Line.md)|  
|**Profile memory allocation and garbage collection**|-   [Collecting Memory Data from an ASP.NET Web Application Using the Profiler Command Line](../vs140/Collecting-Memory-Data-from-an-ASP.NET-Web-Application-by-Using-the-Profiler-Command-Line.md)|  
|**Profile resource contention and thread activity**|-   [Collecting Concurrency Data for an ASP.NET Web Application Using the Profiler Command Line](../vs140/Collecting-Concurrency-Data-for-an-ASP.NET-Web-Application-Using-the-Profiler-Command-Line.md)|  
  
### Sampling Method  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile stand-alone (client) applications**|-   [Collecting Application Statistics for Stand-Alone Applications Using the Profiler Command Line](../vs140/Collecting-Application-Statistics-for-Stand-Alone-Applications-by-Using-the-Profiler-Command-Line.md)|  
|-   **Profile services**|-   [Collecting Application Statistics for Services Using the Profiler Sampling Method](../vs140/Collecting-Application-Statistics-for-Services-by-Using-the-Profiler-Sampling-Method.md)|  
  
### Analyzing Sampling Data Views and Reports  
 [Profiler Sampling Method Data Views](../vs140/Profiler-Sampling-Method-Data-Views.md)