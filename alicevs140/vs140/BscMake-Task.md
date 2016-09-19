---
title: "BscMake Task"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bb98fc67-cad8-43a7-9598-60df6d734db2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BscMake Task
> [!IMPORTANT]
>  bscmake is no longer used by the Visual Studio IDE. Since Visual Studio 2008, browse information is stored automatically in an .sdf file in the Solution folder.  
  
 Wraps the Microsoft Browse Information Maintenance Utility tool (bscmake.exe).  The bscmake.exe tool builds a browse information file (.bsc) from source browser files (.sbr) that are created during compilation. Use the **Object Browser** to view a .bsc file. For more information, see [BSCMAKE Reference](../vs140/BSCMAKE-Reference.md).  
  
## Parameters  
 The following table describes the parameters of the **BscMake** task. Most task parameters correspond to a command-line option.  
  
|Parameter|Description|  
|---------------|-----------------|  
|**AdditionalOptions**|Optional **String** parameter.<br /><br /> A list of options as specified on the command line. For example, "/*option1* /*option2* /*option#*". Use this parameter to specify options that are not represented by any other **BscMake** task parameter.<br /><br /> For more information, see the options in [BSCMAKE Options](../vs140/BSCMAKE-Options.md).|  
|**OutputFile**|Optional **String** parameter.<br /><br /> Specifies a file name that overrides the default output file name.<br /><br /> For more information, see the **/o** option in [BSCMAKE Options](../vs140/BSCMAKE-Options.md).|  
|**PreserveSBR**|Optional **Boolean** parameter.<br /><br /> If `true`, forces a nonincremental build. A full, nonincremental build occurs regardless of whether a .bsc file exists, and prevents .sbr files from being truncated.<br /><br /> For more information, see the **/n** option in [BSCMAKE Options](../vs140/BSCMAKE-Options.md).|  
|**Sources**|Optional **ITaskItem[]** parameter.<br /><br /> Defines an array of MSBuild source file items that can be consumed and emitted by tasks.|  
|**SuppressStartupBanner**|Optional **Boolean** parameter.<br /><br /> If `true`, prevents the display of the copyright and version number message when the task starts.<br /><br /> For more information, see the **/NOLOGO** option in [BSCMAKE Options](../vs140/BSCMAKE-Options.md).|  
|**TrackerLogDirectory**|Optional **String** parameter.<br /><br /> Specifies the directory for the tracker log.|  
  
## Remarks  
  
## See Also  
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)