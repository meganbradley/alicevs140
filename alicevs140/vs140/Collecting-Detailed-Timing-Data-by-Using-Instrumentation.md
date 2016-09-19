---
title: "Collecting Detailed Timing Data by Using Instrumentation"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9deb370-c459-45ac-84d3-14d646590d05
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Collecting Detailed Timing Data by Using Instrumentation
The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools instrumentation method injects profiling code into a copy of a module. The code records each entry, exit, and function call of the functions in the module during a profiling run. The instrumentation method is useful for gathering detailed timing information about a section of your code and for understanding the impact of input and output operations on application performance.  
  
 You can specify the instrumentation method by using one of the following procedures:  
  
-   On the first page of the Profiling Wizard, select **Instrumentation**.  
  
-   On the **Performance Explorer** toolbar, in the **Method** list, click **Instrumentation**.  
  
-   On the **General** page of the properties dialog box for the performance session, select **Instrumentation**.  
  
## Common Tasks  
 You can specify additional options in the *Performance Session***Property Pages** dialog box of the performance session. To open this dialog box:  
  
-   In **Performance Explorer**, right-click the performance session name, and then click **Properties**.  
  
 The tasks in the following table describe options that you can specify in the *Performance Session***Property Pages** dialog box when you profile by using the instrumentation method.  
  
|Task|Related Content|  
|----------|---------------------|  
|On the **General** page, add .NET memory allocation and lifetime data, and specify naming details for the generated profiling data (.vsp) file.|-   [Collecting .NET Memory Allocation and Lifetime Data](../vs140/Collecting-.NET-Memory-Allocation-and-Lifetime-Data.md)<br />-   [How to: Set Profiling Data File Options](../vs140/How-to--Set-Performance-Data-File-Name-Options.md)|  
|On the **Launch** page, if you have multiple .exe projects in your solution.specify the application to start and their start order.|-   [How to: Specify the Binary to Start](../vs140/How-to--Specify-the-Binary-to-Start.md)|  
|On the **Binaries** page, specify a location for the instrumented copies of the modules. By default, the original binaries are moved to a backup folder.|-   [How to: Relocate Instrumented Binaries](../vs140/How-to--Relocate-Instrumented-Binaries.md)|  
|On the **Tier Interaction** page, add ADO.NET call data to the profiling run.|-   [How to: Collect Interaction Data for Multi-Tiered Applications](../vs140/Collecting-tier-interaction-data.md)|  
|On the **Instrumentation** page, exclude small functions from profiling to reduce the profiling overhead, profile JavaScript code in ASP.NET Web pages, and specify commands to run at a command prompt before and after the instrumentation process.|-   [How to: Exclude or Include Short Functions from Instrumentation](../vs140/How-to--Exclude-or-Include-Short-Functions-from-Instrumentation.md)<br />-   [How to: Profile JavaScript (ECMA) Code in Web Pages](../vs140/How-to--Profile-JavaScript-Code-in-Web-Pages.md)<br />-   [How to: Specify Pre- and Post-Instrument Commands](../vs140/How-to--Specify-Pre--and-Post-Instrument-Commands.md)|  
|On the **CPU Counters** page, specify one or more processor performance counters to add to the profiling data.|-   [How to: Collect CPU Counter Data Using the Instrumentation Method](../vs140/How-to--Collect-CPU-Counter-Data.md)|  
|On the **Windows Events** page, select one or more Event Tracing for Windows (ETW) events to collect with the sampling data.|-   [How to: Collect Event Trace (ETW) Data](../vs140/How-to--Collect-Event-Tracing-for-Windows--ETW--Data.md)|  
|On the **Windows Counters** page, specify one or more operating system performance counters to add to the profiling data as marks.|-   [How to: Collect Windows Counter Data](../vs140/How-to--Collect-Windows-Counter-Data.md)|  
|On the **Advanced** page, specify any additional options that you want to pass to the VSInstr instrumentation program, such as options to include or exclude specific functions.|-   [How to: Specify Additional Instrumentation Options](../vs140/How-to--Specify-Additional-Instrumentation-Options.md)<br />-   [How to: Limit Instrumentation to Specific Functions](../vs140/How-to--Limit-Instrumentation-to-Specific-Functions.md)<br />-   [VSInstr](../vs140/VSInstr.md)|