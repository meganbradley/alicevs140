---
title: "Collecting Memory Data from an ASP.NET Web Application by Using the Profiler Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57acf2b0-327a-4c0e-8078-ac2f6d99457d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collecting Memory Data from an ASP.NET Web Application by Using the Profiler Command Line
This section describes the procedures and options for collecting memory allocation and object lifetime data for an ASP.NET Web application by using the **VSPerfCmd** command-line tool.  
  
> [!NOTE]
>  The **VSPerfCmd** tool provides you with complete access to Profiling Tools functionality, including pausing and resuming profiling, and collecting additional data from processor and Windows performance counters. You can also use the  **VSPerfASPNETCmd** command-line tool when you do not need this functionality. Compared with the [VSPerfCmd](../vs140/VSPerfCmd.md) command line tool, no environment variables need to be set, and rebooting the computer is not required. For more information, see [Rapid Web Site Profiling with VSPerfASPNETCmd](../vs140/Rapid-Web-Site-Profiling-with-VSPerfASPNETCmd.md).  
  
## Common Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Attach the profiler to a running ASP.NET application**|-   [How to: Attach the Profiler to an ASP.NET Web Application to Collect Memory Data by Using the Command Line](../vs140/How-to--Attach-the-Profiler-to-an-ASP.NET-Web-Application-to-Collect-Memory-Data-by-Using-the-Command-Line.md)|  
|**Instrument statically compiled binaries**|-   [How to: Instrument a Statically Compiled ASP.NET Web Application and Collect Memory Data by Using the Profiler Command Line](../vs140/How-to--Instrument-a-Statically-Compiled-ASP.NET-Web-Application-and-Collect-Memory-Data-by-Using-the-Profiler-Command-Line.md)|  
|**Instrument dynamically compiled binaries**|-   [How to: Instrument a Dynamically Compiled ASP.NET Web Application and Collect Timing Data by Using the Profiler Command Line](../vs140/How-to--Instrument-a-Dynamically-Compiled-ASP.NET-Web-Application-and-Collect-Memory-Data-by-Using-the-Profiler-Command-Line.md)|  
  
## Related Tasks  
  
### Profiling ASP.NET Web Applications  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile by using the sampling method**|-   [Collecting Application Statistics for ASP.NET Web Applications by Using the Profiler Sampling Method from the Command Line](../vs140/Collecting-Application-Statistics-for-ASP.NET-Web-Applications-Using-the-Profiler-Sampling-Method-from-the-Command-Line.md)|  
|**Profile by using the instrumentation method**|-   [Collecting Detailed Timing Data for an ASP.NET Web Application by Using the Profiler Instrumentation Method from the Command Line](../vs140/Collecting-Detailed-Timing-Data-for-an-ASP.NET-Web-Application-Using-the-Profiler-Instrumentation-Method-from-the-Command-Line.md)|  
|**Profile resource contention and thread activity**|-   [Collecting Concurrency Data for an ASP.NET Web Application Using the Profiler Command Line](../vs140/Collecting-Concurrency-Data-for-an-ASP.NET-Web-Application-Using-the-Profiler-Command-Line.md)|  
  
### Profiling .NET Framework Memory Data  
  
|Task|Related Content|  
|----------|---------------------|  
|**Profile stand-alone (client) applications**|-   [Collecting .NET Framework Memory Data for Stand-Alone Applications by Using the Profiler Command Line](../vs140/Collecting-.NET-Framework-Memory-Data-for-Stand-Alone-Applications-by-Using-the-Profiler-Command-Line.md)|  
|**Profile services**|-   [Collecting .NET Framework Memory Data from Services by Using the Profiler Command Line](../vs140/Collecting-Memory-Data-from-.NET-Framework-Services-by-Using-the-Profiler-Command-Line.md)|  
  
### Analyzing .NET Memory Data Views and Reports  
 [Profiler .NET Memory Data Views](../vs140/.NET-Memory-Data-Views.md)  
  
## Reference  
 [Command-Line Profiling Tools Reference](../vs140/Command-Line-Profiling-Tools-Reference.md)