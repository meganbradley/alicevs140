---
title: "How to: Attach the Profiler to a .NET Framework Stand-Alone Application to Collect Memory Data by Using the Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a869fa4-3c98-4e08-b5d9-f43523059f0e
caps.latest.revision: 35
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Attach the Profiler to a .NET Framework Stand-Alone Application to Collect Memory Data by Using the Command Line
This topic describes how to use [!INCLUDE[vsPreShort](../vs140/includes/vsPreShort_md.md)] Profiling Tools command-line tools to attach the profiler to a running .NET Framework stand-alone (client) application and collect memory data.  
  
> [!NOTE]
>  Command-line tools of the Profiling Tools are located in the \Team Tools\Performance Tools subdirectory of the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] installation directory. On 64-bit computers, both 64-bit and 32-bit versions of the tools are available. To use the profiler command-line tools, you must add the tools path to the PATH environment variable of the Command Prompt window or add it to the command itself. For more information, see [Specifying the Path to Profiling Tools Command Line Tools](../vs140/Specifying-the-Path-to-Profiling-Tools-Command-Line-Tools.md).  
  
 To attach to a .NET Framework application and collect memory data, you must use the [VSPerfCLREnv.cmd](../vs140/VSPerfCLREnv.md) tool to initialize the appropriate environment variables before the target application starts. When the profiler is attached to the application, you can use the **VSPerfCmd.exe** tool to pause and resume data collection.  
  
 To end a profiling session, the profiler must be detached from all profiled processes and the profiler must be explicitly shut down. In most cases, we recommend clearing the profiling environment variables at the end of a session.  
  
## Attaching the Profiler  
  
#### To attach the Profiler to a running .NET Framework application  
  
1.  Open a Command Prompt window.  
  
2.  Initialize the profiling environment variables. Type:  
  
     **VSPerfClrEnv** {**/samplegc** &#124; **/samplegclife**} [**/samplelineoff**]  
  
    -   The **/samplegc** and **/samplegclife** options specify whether to collect only memory allocation data, or to collect both memory allocation and object lifetime data. One and only one option must be specified.  
  
        |Option|Descriptions|  
        |------------|------------------|  
        |**/samplegc**|Collect only memory allocation data.|  
        |**/samplegclife**|Collect both memory allocation and object lifetime data.|  
  
    -   The **/samplelineoff** option disables the collection of source code line number data.  
  
3.  Start the profiler. Type:  
  
     **VSPerfCmd /start:sample /output:** `OutputFile` [`Options`]  
  
    -   The [/start](../vs140/Start.md)**:sample** option initializes the profiler.  
  
    -   The [/output](../vs140/Output.md)**:**`OutputFile` option is required with **/start**. `OutputFile` specifies the name and location of the profiling data (.vsp) file.  
  
     You can use any of the following options with the **/start:sample** option.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/user](../vs140/User--VSPerfCmd-.md) **:**[`Domain`**\\**]`UserName`|Specifies the domain and user name of the account that owns the profiled process. This option is required only if the process is running as a user other than the logged-on user. The process owner is listed in the User Name column on the Processes tab of Windows Task Manager.|  
    |[/crosssession &#124; /cs](../vs140/CrossSession.md)|Enables profiling of processes in other sessions. This option is required if the application is running in a different session. The session idenitifer is listed in the Session ID column on the Processes tab of Windows Task Manager. **/CS** can be specified as an abbreviation for **/crosssession**.|  
    |[/wincounter](../vs140/WinCounter.md) **:** `WinCounterPath`|Specifies a Windows performance counter to be collected during profiling.|  
    |[/automark](../vs140/AutoMark.md) **:** `Interval`|Use with **/wincounter** only. Specifies the number of milliseconds between Windows performance counter collection events. Default is 500 ms.|  
  
4.  If necessary, start the target application in the typical way.  
  
5.  Attach the profiler to the target application. Type:  
  
     **VSPerfCmd**  [/attach](../vs140/Attach.md) **:**{`PID`&#124;`ProcName`} [[/targetclr](../vs140/TargetCLR.md)**:**`Version`]  
  
    -   `PID` specifies the process ID of the target application. `ProcessName` specifies the name of the process. Note that if you specify `ProcessName` and multiple processes that have the same name are running, results are unpredictable. You can view the process IDs of all running processes in Windows Task Manager.  
  
    -   **/targetclr:** `Version` specifies the version of the common language runtime (CLR) to profile when more than one version of the runtime is loaded in an application. Optional.  
  
## Controlling Data Collection  
 When the target application is running, you can control data collection by starting and stopping the writing of data to the file by using **VSPerfCmd.exe** options. Controlling data collection enables you to collect data for a specific part of program execution, such as starting or shutting down the application.  
  
#### To start and stop data collection  
  
-   The following pairs of options start and stop data collection. Specify each option on a separate command line. You can turn data collection on and off multiple times.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/globalon /globaloff](../vs140/GlobalOn-and-GlobalOff.md)|Starts (**/globalon**) or stops (**/globaloff**) data collection for all processes.|  
    |[/processon](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID` [/processoff](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID`|Starts (**/processon**) or stops (**/processoff**) data collection for the process that is specified by the `PID`.|  
    |[/attach](../vs140/Attach.md) **:**{`PID`&#124;`ProcName`} [/detach](../vs140/Detach.md)[**:**{`PID`&#124;`ProcName`}]|**/attach** starts to collect data for the process that is specified by the `PID` or process name (ProcName). **/detach** stops data collection for the specified process or for all processes if a specific process is not specified.|  
  
## Ending the Profiling Session  
 To end a profiling session, the profiler must be detached from all profiled processes and the profiler must be explicitly shut down. You can detach the profiler from an application that was profiled by using the sampling method by closing the application or by calling the **VSPerfCmd /detach** option. You then call the **VSPerfCmd /shutdown** option to turn off the profiler and close the profiling data file. The **VSPerfClrEnv /off** command clears the profiling environment variables.  
  
#### To end a profiling session  
  
1.  Perform one of the following steps to detach the profiler from the target application:  
  
    -   Type **VSPerfCmd /detach**  
  
         -or-  
  
    -   Close the target application.  
  
2.  Shut down the profiler. Type:  
  
     **VSPerfCmd**  [/shutdown](../vs140/Shutdown.md)  
  
3.  (Optional) Clear the profiling environment variables. Type:  
  
     **VSPerfCmd /off**  
  
## See Also  
 [Command-Line Profiling of Stand-Alone Applications](../vs140/Command-Line-Profiling-of-Stand-Alone-Applications.md)   
 [Profiler .NET Memory Data Views](../vs140/.NET-Memory-Data-Views.md)