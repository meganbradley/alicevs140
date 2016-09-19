---
title: "How to: Instrument a .NET Framework Service and Collect Memory Data by Using the Profiler Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2fa072fc-05fe-4420-99c0-51d2ea3ac4ce
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Instrument a .NET Framework Service and Collect Memory Data by Using the Profiler Command Line
This topic describes how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools command-line tools to instrument a [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] service and collect memory usage data. You can collect memory allocation data, or you can collect both memory allocation and object lifetime data.  
  
> [!NOTE]
>  Enhanced security features in Windows 8 and Windows Server 2012 required significant changes in the way the Visual Studio profiler collects data on these platforms. Windows Store apps also require new collection techniques. See [Profiling Windows 8 and Windows Server 2012 applications](../vs140/Performance-Tools-on-Windows-8-and-Windows-Server-2012-applications.md).  
  
> [!NOTE]
>  You cannot profile a service with the instrumentation method if the service cannot be restarted after the computer starts, such a service that start when the operating system starts.  
>   
>  Command-line tools of the Profiling Tools are located in the \Team Tools\Performance Tools subdirectory of the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] installation directory. On 64 bit computers, both 64 bit and 32 bit versions of the tools are available. To use the profiler command-line tools, you must add the tools path to the PATH environment variable of the command prompt window or add it to to the command itself. For more information, see [Specifying the Path to Profiling Tools Command Line Tools](../vs140/Specifying-the-Path-to-Profiling-Tools-Command-Line-Tools.md).  
  
## Starting the Profiling Session  
 To collect performance data from a [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] service, you use the [VSPerfCLREnv.cmd](../vs140/VSPerfCLREnv.md) tool to initialize the appropriate environment variables and the [VSInstr.exe](../vs140/VSInstr.md) tool to create an instrumented copy of the service binary file.  
  
 The computer that hosts the service must be restarted to configure it for profiling. You must also start the service manually from the Service Control Manager. You then start the profiler, and then start the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] service.  
  
 When the instrumented component is executed, memory data is automatically collected to a data file. You can pause and resume data collection during the profiling session.  
  
 To end a profiling session, you close the service and explicitly shut down the profiler. In most cases, we recommend clearing the profiling environment variables at the end of a session.  
  
#### To begin profiling a .NET Framework service  
  
1.  Open a command prompt window.  
  
2.  Use the **VSInstr** tool to generate an instrumented version of the service binary.  
  
3.  Use Service Control Manager to replace the original binary with the instrumented version. Make sure that the service Startup Type is set to Manual.  
  
4.  Initialize the profiling environment variables. Type:  
  
     **VSPerfClrEnv** {**/globaltracegc** &#124; **/globaltracegclife**}  
  
    -   **/globaltracegc** and **/globaltracegclife** enable the collection of memory allocation and object lifetime data.  
  
        |Option|Description|  
        |------------|-----------------|  
        |**/globaltracegc**|Collects memory allocation data only.|  
        |**/globaltracegclife**|Collects memory allocation and object lifetime data.|  
  
5.  Restart the computer.  
  
6.  Open a command prompt window.  
  
7.  Start the profiler. Type:  
  
     **VSPerfCmd**  [/start](../vs140/Start.md) **:trace**  [/output](../vs140/Output.md) **:** `OutputFile` [`Options`]  
  
    -   The **/start: contention** option initializes the profiler.  
  
    -   The **/output:**`OutputFile` option is required with **/start**. `OutputFile` specifies the name and location of the profiling data (.vsp) file.  
  
     You can use any of the following options with the **/start:sample** option.  
  
    > [!NOTE]
    >  The **/user** and **/crosssession** options are usually required for services.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/user](../vs140/User--VSPerfCmd-.md) **:**[`Domain`**\\**]`UserName`|Specifies the domain and user name of the account that owns the ASP.NET worker process. This option is required if the process is running as a user other than the logged on user. The process owner is listed in the User Name column on the Processes tab of Windows Task Manager.|  
    |[/crosssession](../vs140/CrossSession.md)|Enables profiling of processes in other logon sessions. This option is required if the ASP.NET application is running in a different session. The session id is listed in the Session ID column on the the Processes tab of Windows Task Manager. **/CS** can be specified as an abbreviation for **/crosssession**.|  
    |[/waitstart](../vs140/WaitStart.md)[**:**`Interval`]|Specifies the number of seconds to wait for the profiler to initialize before it returns an error. If `Interval` is not specified, the profiler waits indefinitely. By default, **/start** returns immediately.|  
    |[/globaloff](../vs140/GlobalOn-and-GlobalOff.md)|To start the profiler with data collection paused, add the **/globaloff** option to the **/start** command line. Use **/globalon** to resume profiling.|  
    |[/counter](../vs140/Counter.md) **:** `Config`|Collects information from the processor performance counter specified in Config. Counter information is added to the data collected at each profiling event.|  
    |[/wincounter](../vs140/WinCounter.md) **:** `WinCounterPath`|Specifies a Windows performance counter to be collected during profiling.|  
    |[/automark](../vs140/AutoMark.md) **:** `Interval`|Use with **/wincounter** only. Specifies the number of milliseconds between Windows performance counter collection events. Default is 500 ms.|  
    |[/events](../vs140/Events--VSPerfCmd-.md) **:** `Config`|Specifies an Event Tracing for Windows (ETW) event to be collected during profiling. ETW events are collected in a separate (.etl) file.|  
  
8.  If necessary, start the service.  
  
9. Attach the profiler to the service. Type:  
  
     **VSPerfCmd /attach:** `PID`&#124;`ProcessName`  
  
    -   Specify the the process ID or process name of the service. You can view the process IDs and names of all running processes in Windows Task Manager.  
  
## Controlling Data Collection  
 While the service is running, you can control data collection by starting and stopping the writing of data to the file with **VSPerfCmd.exe** options. Controlling data collection enables you to collect data for a specific part of program execution, such as starting or shutting down the application.  
  
#### To start and stop data collection  
  
-   The following pairs of **VSPerfCmd** options start and stop data collection. Specify each option on a separate command line. You can turn data collection on and off multiple times.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/globalon /globaloff](../vs140/GlobalOn-and-GlobalOff.md)|Starts (**/globalon**) or stops (**/globaloff**) data collection for all processes.|  
    |[/processon](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID` [/processoff](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID`|Starts (**/processon**) or stops (**/processoff**) data collection for the process specified by the process ID (`PID`).|  
    |[/threadon](../vs140/ThreadOn-and-ThreadOff.md) **:** `TID` [/threadoff](../vs140/ThreadOn-and-ThreadOff.md) **:** `TID`|Starts (**/threadon**) or stops (**/threadoff**) data collection for the thread specified by the thread ID (`TID`).|  
  
## Ending the Profiling Session  
 To end a profiling session, close the application that is running the instrumented component, then start the **VSPerfCmd** [/shutdown](../vs140/Shutdown.md) option to turn the profiler off and close the profiling data file. The **VSPerfClrEnv /globaloff** command clears the profiling environment variables.  
  
#### To end a profiling session  
  
1.  Stop the service from Service Control Manager.  
  
2.  Shut down the profiler. Type:  
  
     **VSPerfCmd /shutdown**  
  
3.  When you have completed all profiling, clear the profiling environment variables. Type:  
  
     **VSPerfClrEnv /globaloff**  
  
     Replace the instrumented module with the original. If necessary, reconfigure the Startup Type of the service.  
  
4.  Restart the computer.  
  
## See Also  
 [Command-Line Profiling of Services](../vs140/Command-Line-Profiling-of-Services.md)   
 [Profiler .NET Memory Data Views](../vs140/.NET-Memory-Data-Views.md)