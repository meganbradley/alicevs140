---
title: "How to: Create a Profiling Tools Call Trace Report"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7640520a-7d3c-456c-b184-872a5d2f82f3
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Profiling Tools Call Trace Report
The  *call trace report* for the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Profiling Tools lists timing information for each entry and exit point to your application's functions and each call to other functions by your function. Call trace reports are available for profiling data only if it was collected with the instrumentation method.  
  
> [!NOTE]
>  You cannot display call trace reports in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. You must use the **VSPerfReport** command-line tool to generate a comma-separated value (.csv) or Xml file. For more information about this tool, see [VSPerfReport](../vs140/VSPerfReport.md).  
  
### To create a call trace report  
  
1.  Open a **Command Prompt**ine window.  
  
2.  At the command prompt, type the following command:  
  
     *ToolsPath* **VSPerfReport** *VSPFile*  **/CallTrace [/Xml]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|The path of Profiling Tools command line tools. For more information, see [Specifying the Path to Profiling Tools Command Line Tools](../vs140/Specifying-the-Path-to-Profiling-Tools-Command-Line-Tools.md).|  
    |*VSPFile*|The profiling data (.vsp or .vsps) file. Full and partial paths are accepted.|  
    |Xml|Generates an Xml formatted report.|  
  
## See Also  
 [How to: Enable Event Trace Providers](../vs140/How-to--Collect-Event-Tracing-for-Windows--ETW--Data.md)   
 [Profiling Tools APIs](../vs140/Profiling-Tools-APIs.md)