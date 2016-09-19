---
title: "Configuring Performance Sessions"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e1c3ba41-ffca-4edf-9a7f-8a5a9244ef9b
caps.latest.revision: 38
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Configuring Performance Sessions
By using [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools, you can collect a wide variety of performance data for a large number of application types. This section shows you how to use the Performance Wizardand properties of the performance session and target binary to configure Profiling Tools to collect the data that interests you. Profiling Tools configuration properties can also be used to control how much data is collected in a profiling run. For more information, see [Controlling Data Collection](../vs140/Controlling-Data-Collection.md).  
  
> [!NOTE]
>  In many cases, using the default properties of the Performance Wizard is an effective way of collecting profiling data. For more information, see [How to: Profile with the Performance Wizard and Profiler Defaults](../vs140/Beginners-Guide-to-Performance-Profiling.md) and [Getting Started with Profiling Tools](../vs140/Getting-Started-with-Performance-Tools.md).  
  
## Common Tasks  
  
|Task|Related Content|  
|----------|---------------------|  
|**Set the basic profiling options:** You should configure [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] to use the Microsoft symbol server. This will make sure that you have access to symbols, such as function and parameter names, for the current version of Windows and other Microsoft applications. You can also specify other general options before a profiling session starts, such as system permissions to the profiling tools and the names of profiling data files.|-   [How to: Reference Windows Symbol Information](../vs140/How-to--Reference-Windows-Symbol-Information.md)<br />-   [How to: Serialize Symbol Information](../vs140/How-to--Serialize-Symbol-Information.md)<br />-   [How to: Set the Current Profiling Session](../vs140/How-to--Set-the-Current-Session.md)<br />-   [How to: Set Profiling Permissions](../vs140/How-to--Set-Permissions.md)<br />-   [How to: Set Profiling Data File Name Options](../vs140/How-to--Set-Performance-Data-File-Name-Options.md)|  
|**Specify the data that you want to collect:** The procedures that you use to configure a profiling session depend on the type of target application that you want to profile and the type of performance data that you want to collect.|-   [How to: Choose Collection Methods](../vs140/How-to--Choose-Collection-Methods.md)<br />-   [Collecting Performance Statistics by Using Sampling](../vs140/Collecting-Performance-Statistics-by-Using-Sampling.md)<br />-   [Collecting .NET Memory Allocation and Lifetime Data](../vs140/Collecting-.NET-Memory-Allocation-and-Lifetime-Data.md)<br />-   [Collecting Detailed Timing Data by Using Instrumentation](../vs140/Collecting-Detailed-Timing-Data-by-Using-Instrumentation.md)<br />-   [How to: Profile JavaScript (ECMA) Code in Web Pages](../vs140/How-to--Profile-JavaScript-Code-in-Web-Pages.md)<br />-   [Collecting Thread and Process Concurrency Data](../vs140/Collecting-Thread-and-Process-Concurrency-Data.md)<br />-   [Collecting Additional Performance Data](../vs140/Collecting-Additional-Performance-Data.md)|  
|**Set advanced configuration options:** When you profile .NET Framework applications that load multiple versions of the common language run-time (CLR), you can specify which version to profile. When you have multiple .exe files in a performance session, you can set the start order of the binaries.|-   [How to: Specify the .NET Framework Runtime to Profile in Side by Side Scenarios](../vs140/How-to--Specify-the-.NET-Framework-Runtime.md)<br />-   [How to: Specify the Binary to Start](../vs140/How-to--Specify-the-Binary-to-Start.md)|  
  
## Related Sections  
 [Controlling Data Collection](../vs140/Controlling-Data-Collection.md)  
  
## See Also  
 [Analyzing Application Performance using Profiling Tools](../vs140/Performance-Explorer.md)