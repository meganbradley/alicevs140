---
title: "How to: Instrument a Statically Compiled ASP.NET Web Application and Collect Memory Data by Using the Profiler Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea1dcb7c-1dc3-49ff-9418-8795b5b3d3bc
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Instrument a Statically Compiled ASP.NET Web Application and Collect Memory Data by Using the Profiler Command Line
This topic describes how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools command-line tools to instrument a pre-compiled [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] Web component or Web site and collect .NET memory allocation, object lifetime, and detailed timing data.  
  
> [!NOTE]
>  Command-line tools of the Profiling Tools are located in the \Team Tools\Performance Tools subdirectory of the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] installation directory. On 64 bit computers, both 64 bit and 32 bit versions of the tools are available. To use the profiler command-line tools, you must add the tools path to the PATH environment variable of the command prompt window or add it to to the command itself. For more information, see [Specifying the Path to Profiling Tools Command Line Tools](../vs140/Specifying-the-Path-to-Profiling-Tools-Command-Line-Tools.md).  
  
 To collect data from a [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] Web component by using the instrumentation method, you use the [VSInstr.exe](../vs140/VSInstr.md) tool to generate an instrumented version of the component. On the computer that hosts the component, you replace the non-instrumented version of the component with the instrumented version. You then use the [VSPerfCLREnv.cmd](../vs140/VSPerfCLREnv.md) tool to initialize the global profiling environment variables and restart the host computer. You then start the profiler.  
  
 When the instrumented component is executed, timing data is automatically collected to a data file. You can pause and resume data collection during the profiling session.  
  
 To end a profiling session, you close the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process that hosts the component and then explicitly shut down the profiler. In most cases, we recommend clearing the profiling environment variables at the end of a session.  
  
## Starting to Profile  
  
#### To instrument an ASP.NET Web component and start profiling  
  
1.  Use the **VSInstr** tool to generate an instrumented version of the target application. If necessary, replace the application binaries on the ASP.NET host computer with the instrumented binaries.  
  
2.  Open a command prompt window  
  
3.  Initialize the .NET profiling environment variables. In a command prompt window, type:  
  
     **VSPerfClrEnv /globaltracegc**  
  
     -or-  
  
     **VSPerfClrEnv /globaltracegclife**  
  
    -   **/globaltracegc** collects .NET memory allocation and timing data.  
  
    -   **/globaltracegclife** collects .NET memory allocation, object lifetime, and detailed timing data.  
  
4.  Restart the computer.  
  
5.  Open a command prompt window.  
  
6.  Start the profiler. In a command prompt window, type:  
  
     **VSPerfCmd /start:trace /output:** `OutputFile` [`Options`]  
  
    -   The [/start](../vs140/Start.md)**:trace** option initializes the profiler.  
  
    -   The [/output](../vs140/Output.md)**:**`OutputFile` option is required with **/start**. `OutputFile` specifies the name and location of the profiling data (.vsp) file.  
  
     You can use any of the following options with the **/start:trace** option.  
  
    > [!NOTE]
    >  The **/user** and **/crosssession** options are usually required for ASP.NET applications.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/user](../vs140/User--VSPerfCmd-.md) **:**[`Domain`**\\**]`UserName`|Specifies the optional domain and user name of the account that owns the ASP.NET worker process. This option is required if the process is running as a user that is different than the logged on user.The name is listed in the User Name column on the Processes tab of Windows Task Manager.|  
    |[/crosssession](../vs140/CrossSession.md)|Enables profiling of processes in other sessions. This option is required if the application is running in a different session. The session id is listed in the Session ID column on the the Processes tab of Windows Task Manager. **/CS** can be specified as an abbreviation for **/crosssession**.|  
    |[/wincounter](../vs140/WinCounter.md) **:** `WinCounterPath`|Specifies a Windows performance counter to be collected during profiling.|  
    |[/automark](../vs140/AutoMark.md) **:** `Interval`|Use with **/wincounter** only. Specifies the number of milliseconds between Windows performance counter collection events. Default is 500 ms.|  
    |[/events](../vs140/Events--VSPerfCmd-.md) **:** `Config`|Specifies an Event Tracing for Windows (ETW) event to be collected during profiling. ETW events are collected in a separate (.etl) file.|  
    |[/globaloff](../vs140/GlobalOn-and-GlobalOff.md)|To start the profiler with data collection paused, add the **/globaloff** option to the **/start** command line. Use **/globalon** to resume profiling.|  
  
7.  Open the Web site that contains the instrumented component.  
  
## Controlling Data Collection  
 While the target application is running, you can control data collection by starting and stopping the writing of data to the file by using **VSPerfCmd.exe** options. Controlling data collection enables you to collect data for a specific part of program execution, such as starting or shutting down the application.  
  
#### To start and stop data collection  
  
-   The following pairs of options start and stop data collection. Specify each option on a separate command line. You can turn data collection on and off multiple times.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/globalon /globaloff](../vs140/GlobalOn-and-GlobalOff.md)|Starts (**/globalon**) or stops (**/globaloff**) data collection for all processes.|  
    |[/processon](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID` [/processoff](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID`|Starts (**/processon**) or stops (**/processoff**) data collection for the process specified by the process ID (`PID`).|  
    |[/threadon](../vs140/ThreadOn-and-ThreadOff.md) **:** `TID` [/threadoff](../vs140/ThreadOn-and-ThreadOff.md) **:** `TID`|Starts (**/threadon**) or stops (**/threadoff**) data collection for the thread specified by the thread ID (`TID`).|  
  
## Ending the Profiling Session  
 To end a profiling session, close the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] Web application, and then use the Internet Information Services (IIS) **IISReset** command to close the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process. Call the **VSPerfCmd** [/shutdown](../vs140/Shutdown.md) option to turn the profiler off and close the profiling data file. The **VSPerfClrEnv /globaloff** command clears the profiling environment variables. You must restart the computer for the new environment settings to be applied.  
  
#### To end a profiling session  
  
1.  Close the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] Web application.  
  
2.  Close the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process. Type:  
  
     **IISReset /stop**  
  
3.  Shut down the profiler. Type:  
  
     **VSPerfCmd /shutdown**  
  
4.  (Optional). Clear the profiling environment variables. Type:  
  
     **VSPerfCmd /globaloff**  
  
5.  Restart the computer. If necessary, restart IIS. Type:  
  
     **IISReset /start**  
  
## See Also  
 [Command-Line Profiling of ASP.NET Applications](../vs140/Command-Line-Profiling-of-ASP.NET-Web-Applications.md)   
 [Profiler .NET Memory Data Views](../vs140/.NET-Memory-Data-Views.md)