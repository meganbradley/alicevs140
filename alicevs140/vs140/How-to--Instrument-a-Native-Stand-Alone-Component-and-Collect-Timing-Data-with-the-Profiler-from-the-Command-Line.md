---
title: "How to: Instrument a Native Stand-Alone Component and Collect Timing Data with the Profiler from the Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 36883074-9be8-4e90-a66f-7e87f21fcd30
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Instrument a Native Stand-Alone Component and Collect Timing Data with the Profiler from the Command Line
This topic describes how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools command-line tools to instrument a native component such as a C++ .exe or .dll file, and to collect detailed timing data.  
  
> [!NOTE]
>  Command-line tools of the Profiling Tools are located in the \Team Tools\Performance Tools subdirectory of the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] installation directory. On 64-bit computers, both 64-bit and 32-bit versions of the tools are available. To use the profiler command-line tools, you must add the tools path to the PATH environment variable of the Command Prompt window or add it to the command itself. For more information, see [Specifying the Path to Profiling Tools Command Line Tools](../vs140/Specifying-the-Path-to-Profiling-Tools-Command-Line-Tools.md).  
  
 To collect detailed timing data from a component by using the instrumentation method, you use the [VSInstr.exe](../vs140/VSInstr.md) tool to generate an instrumented version of the component. You then start the profiler. When the instrumented component is executed, timing data is automatically collected to a data file. You can pause and resume data collection during the profiling session.  
  
 To end a profiling session, you close the target application and then explicitly shut down the profiler.  
  
## Starting the Profiling Session  
  
#### To start profiling by using the instrumentation method  
  
1.  Open a Command Prompt window.  
  
2.  Use the **VSInstr** tool to generate an instrumented version of the target application.  
  
3.  Start the profiler. Type:  
  
     **VSPerfCmd /start:trace /output:** `OutputFile` [`Options`]  
  
    -   The [/start](../vs140/Start.md)**:trace** option initializes the profiler.  
  
    -   The [/output](../vs140/Output.md)**:**`OutputFile` option is required with **/start**. `OutputFile` specifies the name and location of the profiling data (.vsp) file.  
  
     You can use one or more of the following options with the **/start:trace** option.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/user](../vs140/User--VSPerfCmd-.md) **:**[`Domain`**\\**]`UserName`|Specifies the domain and user name of the account that owns the profiled process. This option is required only if the process is running as a user other than the logged-on user. The process owner is listed in the User Name column on the Processes tab of Windows Task Manager.|  
    |[/crosssession](../vs140/CrossSession.md)|Enables profiling of processes in other sessions. This option is required if the application is running in a different session. The session idenitifier is listed in the Session ID column on the Processes tab of Windows Task Manager. **/CS** can be specified as an abbreviation for **/crosssession**.|  
    |[/globaloff](../vs140/GlobalOn-and-GlobalOff.md)|Starts the profiler with data collection paused. Use [/globalon](../vs140/GlobalOn-and-GlobalOff.md) to resume profiling.|  
    |[/counter](../vs140/Counter.md) **:** `Config`|Collects information from the processor performance counter that is specified in `Config`. Counter information is added to the data that is collected at each profiling event.|  
    |[/wincounter](../vs140/WinCounter.md) **:** `WinCounterPath`|Specifies a Windows performance counter to be collected during profiling.|  
    |[/automark](../vs140/AutoMark.md) **:** `Interval`|Use with **/wincounter** only. Specifies the number of milliseconds between Windows performance counter collection events. Default is 500 ms.|  
    |[/events](../vs140/Events--VSPerfCmd-.md) **:** `Config`|Specifies an Event Tracing for Windows (ETW) event to be collected during profiling. ETW events are collected in a separate (.etl) file.|  
  
4.  Start the target application in the typical way.  
  
## Controlling Data Collection  
 When the target application is running, you can control data collection by starting and stopping the writing of data to the file by using **VSPerfCmd.exe** options. Controlling data collection enables you to collect data for a specific part of program execution, such as starting or shutting down the application.  
  
#### To start and stop data collection  
  
-   The following pairs of options start and stop data collection. Specify each option on a separate command line. You can turn data collection on and off multiple times.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/globalon /globaloff](../vs140/GlobalOn-and-GlobalOff.md)|Starts (**/globalon**) or stops (**/globaloff**) data collection for all processes.|  
    |[/processon](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID` [/processoff](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID`|Starts (**/processon**) or stops (**/processoff**) data collection for the process that is specified by the process ID (`PID`).|  
    |[/threadon](../vs140/ThreadOn-and-ThreadOff.md) **:** `TID` [/threadoff](../vs140/ThreadOn-and-ThreadOff.md) **:** `TID`|Starts (**/threadon**) or stops (**/threadoff**) data collection for the thread that is specified by the thread ID (`TID`).|  
  
## Ending the Profiling Session  
 To end a profiling session, close the application that is running the instrumented component, and then call the **VSPerfCmd** [/shutdown](../vs140/Shutdown.md) option to turn off the profiler and close the profiling data file.  
  
#### To end a profiling session  
  
1.  Close the target application.  
  
2.  Shut down the profiler. Type:  
  
     **VSPerfCmd /shutdown**  
  
## See Also  
 [Command-Line Profiling of Stand-Alone Applications](../vs140/Command-Line-Profiling-of-Stand-Alone-Applications.md)   
 [Profiler Instrumentation Method Data Views](../vs140/Instrumentation-Method-Data-Views.md)