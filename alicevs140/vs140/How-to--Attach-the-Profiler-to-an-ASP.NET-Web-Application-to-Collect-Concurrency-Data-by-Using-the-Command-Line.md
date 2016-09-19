---
title: "How to: Attach the Profiler to an ASP.NET Web Application to Collect Concurrency Data by Using the Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0e215fdd-55f8-43ef-9534-06542eefe223
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Attach the Profiler to an ASP.NET Web Application to Collect Concurrency Data by Using the Command Line
This topic describes how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools command-line tools to attach the Profiler to an ASP.NET application and collect process and thread concurrency data.  
  
 Command-line tools of the Profiling Tools are located in the \Team Tools\Performance Tools subdirectory of the Visual Studio installation directory. On 64-bit computers, both 64-bit and 32-bit versions of the tools are available. To use the profiler at a command prompt, you must add the tools path to the PATH environment variable of the **Command Prompt** window or add it to the command itself. For more information, see [Specifying the Path to Profiling Tools Command Line Tools](../vs140/Specifying-the-Path-to-Profiling-Tools-Command-Line-Tools.md).  
  
 To collect concurrency data, you attach the profiler to the ASP.NET worker process that hosts your Web site. While the profiler is attached to the application, you can pause and resume data collection. To end a profiling session, the Profiler must no longer be attached to the application, and the Profiler must be explicitly shut down. In most cases, you should clear the profiling environment variables at the end of a session.  
  
## Attaching the Profiler  
  
#### To attach the Profiler to a ASP.NET application  
  
1.  Start the profiler by typing the following command:  
  
     [VSPerfCmd](../vs140/VSPerfCmd.md) **/start:concurrency /output:** `OutputFile` [`Options`]  
  
    -   The [/start](../vs140/Start.md) option initializes the profiler to collect resource contention data.  
  
    -   The [/output](../vs140/Output.md)**:**`OutputFile` option is required with **/start**. `OutputFile` specifies the name and location of the profiling data (.vsp) file.  
  
     You can use any option in the following table with the **/start** option.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/user](../vs140/User--VSPerfCmd-.md) **:**[`Domain\`]`UserName`|Specifies the optional domain and user name of the account to be granted access to the profiler.|  
    |[/crosssession](../vs140/CrossSession.md)|Enables profiling of processes in other logon sessions.|  
    |[/wincounter](../vs140/WinCounter.md) **:** `WinCounterPath`|Specifies a Windows performance counter to be collected during profiling.|  
    |[/automark](../vs140/AutoMark.md) **:** `Interval`|Use with **/wincounter** only. Specifies the number of milliseconds between Windows performance counter collection events. The default value is 500.|  
    |[/events](../vs140/Events--VSPerfCmd-.md) **:** `Config`|Specifies an Event Tracing for Windows (ETW) event to be collected during profiling. ETW events are collected in a separate (.etl) file.|  
  
2.  Start the ASP.NET application in the typical way.  
  
3.  Attach the profiler to the ASP.NET worker process by typing the following command:**VSPerfCmd /attach:**`PID` [**/targetclr:**`Version`]  
  
    -   `PID` specifies the ID or name of the ASP.NET worker process. You can view the process IDs of all running processes in Windows Task Manager.  
  
    -   [/targetclr](../vs140/TargetCLR.md) **:** `Version` specifies the version of the common language runtime (CLR) to profile when more than one version of the runtime is loaded in an application. This parameter is optional.  
  
## Controlling Data Collection  
 While the application is running, you can control data collection by starting and stopping the writing of data to the file by using VSPerfCmd.exe options. By controlling data collection, you can collect data for a specific part of program execution, such as the starting or shutting down of the application.  
  
#### To start and stop data collection  
  
-   The pairs of VSPerfCmd options in the following table start and stop data collection. Specify each option on a separate command line. You can turn data collection on and off multiple times.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/globalon /globaloff](../vs140/GlobalOn-and-GlobalOff.md)|Starts (**/globalon**) or stops (**/globaloff**) data collection for all processes.|  
    |[/processon](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID`  [processoff](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID`|Starts (**/processon**) or stops (**/processoff**) data collection for the process that the process ID (`PID`) specifies.|  
    |[/attach](../vs140/Attach.md) **:**{`PID`&#124;`ProcName`} [/detach](../vs140/Detach.md)[**:**{`PID`&#124;`ProcName`}]|**/attach** starts to collect data for the process that the process ID (`PID`) or process name (*ProcName*) specifies. **/detach** stops data collection for the specified process or for all processes if no process is specified.|  
  
## Ending the Profiling Session  
 To end a profiling session, the profiler must not be collecting data. You can stop collecting data from a application that is profiled with the concurrency method by restarting the ASP.NET worker process or by invoking the **VSPerfCmd /detach** option. You then invoke the **VSPerfCmd /shutdown** option to turn off the profiler and close the profiling data file. The **VSPerfClrEnv /globaloff** command clears the profiling environment variables, but the system configuration is not reset until the computer is restarted.  
  
#### To end a profiling session  
  
1.  Detach the profiler from the target application by closing it or by typing the following at a command prompt:  
  
     **VSPerfCmd /detach**  
  
2.  Shut down the profiler by typing the following command at a command prompt:  
  
     **VSPerfCmd**  [/shutdown](../vs140/Shutdown.md)  
  
## See Also  
 [Command-Line Profiling of ASP.NET Web Applications](../vs140/Command-Line-Profiling-of-ASP.NET-Web-Applications.md)   
 [Rapid Web Site Profiling with VSPerfASPNETCmd](../vs140/Rapid-Web-Site-Profiling-with-VSPerfASPNETCmd.md)