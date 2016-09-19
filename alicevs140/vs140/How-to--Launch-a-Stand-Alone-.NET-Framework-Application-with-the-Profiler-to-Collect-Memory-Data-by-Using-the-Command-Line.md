---
title: "How to: Launch a Stand-Alone .NET Framework Application with the Profiler to Collect Memory Data by Using the Command Line"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3bc53041-91b7-4ad0-8413-f8bf2c4b3f5e
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Launch a Stand-Alone .NET Framework Application with the Profiler to Collect Memory Data by Using the Command Line
This topic describes how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools command-line tools to start a .NET Framework stand-alone (client) application and collect memory data.  
  
 A profiling session has three parts:  
  
-   Starting the application by using the profiler.  
  
-   Collecting profiling data.  
  
-   Ending the profiling session.  
  
> [!NOTE]
>  Command-line tools of the Profiling Tools are located in the \Team Tools\Performance Tools subdirectory of the [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] installation directory. On 64-bit computers, both 64-bit and 32-bit versions of the tools are available. To use the profiler command-line tools, you must add the tools path to the PATH environment variable of the Command Prompt window or add it to the command itself. For more information, see [Specifying the Path to Profiling Tools Command Line Tools](../vs140/Specifying-the-Path-to-Profiling-Tools-Command-Line-Tools.md).  
  
## Starting the Application with the Profiler  
 To start a target application by using the profiler, you use the **VSPerfCmd.exe/start** and **/launch** options to initialize the profiler and start the application. You can specify **/start** and **/launch** and their respective options on one command line.  
  
 You can also add the **/globaloff** options to pause data collection at the start of the target application. You then use **/globalon** to start to collect data.  
  
#### To start an application by using the Profiler  
  
1.  Open a Command Prompt window.  
  
2.  Start the profiler. Type:  
  
     **VSPerfCmd /start:sample /output:** `OutputFile` [`Options`]  
  
    -   The [/start](../vs140/Start.md)**:sample** option initializes the profiler.  
  
    -   The [/output](../vs140/Output.md)**:**`OutputFile` option is required with **/start**. `OutputFile` specifies the name and location of the profiling data (.vsp) file.  
  
     You can use any of the following options with the **/start:sample** option.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/wincounter](../vs140/WinCounter.md) **:** `WinCounterPath`|Specifies a Windows performance counter to be collected during profiling.|  
    |[/automark](../vs140/AutoMark.md) **:** `Interval`|Use with **/wincounter** only. Specifies the number of milliseconds between Windows performance counter collection events. Default is 500 ms.|  
  
3.  Start the target application. Type:  
  
     **VSPerfCmd**  [/launch](../vs140/Launch.md) **:** `appName` **/gc:**{**allocation**&#124;**lifetime**}[`Options`]  
  
    -   The [/gc](../vs140/GC--VSPerfCmd-.md)**:**`Keyword` option is required to collect .NET Framework memory data. The keyword parameter specifies whether to collect memory allocation data, or to collect both memory allocation and object lifetime data.  
  
        |Keyword|Description|  
        |-------------|-----------------|  
        |**allocation**|Collect memory allocation data only.|  
        |**lifetime**|Collect both memory allocation and object lifetime data.|  
  
     You can use any of the following options with the **/launch** option.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/args](../vs140/Args.md) **:** `Arguments`|Specifies a string that contains the command-line arguments to be passed to the target application.|  
    |[/console](../vs140/Console.md)|Starts the target command-line application in a separate window.|  
    |[/events](../vs140/Events--VSPerfCmd-.md) **:** `Config`|Specifies an Event Tracing for Windows (ETW) event to be collected during profiling. ETW events are collected in a separate (.etl) file.|  
    |[/targetclr](../vs140/TargetCLR.md) **:** `Version`|Specifies the version of the common language runtime (CLR) to profile when more than one version of the runtime is loaded in an application.|  
  
## Controlling Data Collection  
 When the target application is running, you can control data collection by starting and stopping the writing of data to the file by using **VSPerfCmd.exe** options. Controlling data collection enables you to collect data for a specific part of program execution, such as starting or shutting down the application.  
  
#### To start and stop data collection  
  
-   The following pairs of options start and stop data collection. Specify each option on a separate command line. You can turn data collection on and off multiple times.  
  
    |Option|Description|  
    |------------|-----------------|  
    |[/globalon /globaloff](../vs140/GlobalOn-and-GlobalOff.md)|Starts (**/globalon**) or stops (**/globaloff**) data collection for all processes.|  
    |[/processon](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID` [processoff](../vs140/ProcessOn-and-ProcessOff.md) **:** `PID`|Starts (**/processon**) or stops (**/processoff**) data collection for the process that is specified by the process ID (`PID`).|  
    |[/attach](../vs140/Attach.md) **:** `PID` [/detach](../vs140/Detach.md)|**/attach** starts to collect data for the process that is specified by `PID` (the process ID). **/detach** stops data collection for all processes.|  
  
-   You can also use the **VSPerfCmd.exe**[/mark](../vs140/Mark.md) option to insert a profiling mark into the data file. The **/mark** command adds an identifier, a time stamp, and an optional user-defined text string. Marks can be used to filter the data.  
  
## Ending the Profiling Session  
 To end a profiling session, the profiler must be detached from all profiled processes and the profiler must be explicitly shut down. You can detach the profiler from an application that was profiled by using the sampling method by closing the application or by calling the **VSPerfCmd /detach** option. You then call the **VSPerfCmd /shutdown** option to turn off the profiler and close the profiling data file. The **VSPerfClrEnv /off** command clears the profiling environment variables.  
  
#### To end a profiling session  
  
1.  Perform one of the following steps to detach the profiler from the target application:  
  
    -   Close the target application.  
  
         -or-  
  
    -   Type **VSPerfCmd /detach**  
  
2.  Shut down the profiler. Type:  
  
     **VSPerfCmd**  [/shutdown](../vs140/Shutdown.md)  
  
## See Also  
 [Command-Line Profiling of Stand-Alone Applications](../vs140/Command-Line-Profiling-of-Stand-Alone-Applications.md)   
 [Profiler .NET Memory Data Views](../vs140/.NET-Memory-Data-Views.md)