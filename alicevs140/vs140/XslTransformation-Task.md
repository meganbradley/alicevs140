---
title: "XslTransformation Task"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6f3a7d81-3ae3-4703-9a06-870b32b69d80
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# XslTransformation Task
Transforms an XML input by using an XSLT or compiled XSLT and outputs to an output device or a file.  
  
## Parameters  
 The following table describes the parameters of the `XslTransformation` task.  
  
|Parameter|Description|  
|---------------|-----------------|  
|`OutputPaths`|Required <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False>`[]` parameter.<br /><br /> Specifies the output files for the XML transformation.|  
|`Parameters`|Optional `String` parameter.<br /><br /> Specifies the parameters to the XSLT Input document.|  
|`XmlContent`|Optional `String` parameter.<br /><br /> Specifies the XML input as a string.|  
|`XmlInputPaths`|Optional <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False>`[]` parameter.<br /><br /> Specifies the XML input files.|  
|`XslCompiledDllPath`|Optional <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False> parameter.<br /><br /> Specifies the compiled XSLT.|  
|`XslContent`|Optional `String` parameter.<br /><br /> Specifies the XSLT input as a string.|  
|`XslInputPath`|Optional <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False> parameter.<br /><br /> Specifies the XSLT input file.|  
  
## Remarks  
 In addition to having the parameters that are listed in the table, this task inherits parameters from the <xref:Microsoft.Build.Tasks.TaskExtension?qualifyHint=False> class, which itself inherits from the <xref:Microsoft.Build.Utilities.Task?qualifyHint=False> class. For a list of these additional parameters and their descriptions, see [TaskExtension Base Class](../Topic/TaskExtension%20Base%20Class.md).  
  
## See Also  
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)