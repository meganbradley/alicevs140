---
title: "CreateVisualBasicManifestResourceName Task"
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
ms.assetid: 251c47b9-de32-414b-a138-bf45290af12e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CreateVisualBasicManifestResourceName Task
Creates a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]-style manifest name from a given .resx file name or other resource.  
  
## Parameters  
 The following table describes the parameters of the [CreateVisualBasicManifestResourceName Task](../vs140/CreateVisualBasicManifestResourceName-Task.md).  
  
|Parameter|Description|  
|---------------|-----------------|  
|`ManifestResourceNames`|<xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False> `[]` output read-only parameter.<br /><br /> The resulting manifest names.|  
|`ResourceFiles`|Required `String` parameter.<br /><br /> The name of the resource file from which to create the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] manifest name.|  
|`RootNamespace`|Optional `String` parameter.<br /><br /> The root namespace of the resource file, typically taken from the project file. May be `null`.|  
|`PrependCultureAsDirectory`|Optional `Boolean` parameter.<br /><br /> If `true`, the culture name is added as a directory name just before the manifest resource name. Default value is `true`.|  
|`ResourceFilesWithManifestResourceNames`|Optional read-only `String` output parameter.<br /><br /> Returns the name of the resource file that now includes the manifest resource name.|  
  
## Remarks  
 The [CreateVisualBasicManifestResourceName Task](../vs140/CreateVisualBasicManifestResourceName-Task.md) determines the appropriate manifest resource name to assign to a given .resx or other resource file. The task provides a logical name to a resource file, and then attaches it to an output parameter as metadata.  
  
 In addition to the parameters listed above, this task inherits parameters from the <xref:Microsoft.Build.Tasks.TaskExtension?qualifyHint=False> class, which itself inherits from the <xref:Microsoft.Build.Utilities.Task?qualifyHint=False> class. For a list of these additional parameters and their descriptions, see [TaskExtension Base Class](../Topic/TaskExtension%20Base%20Class.md).  
  
## See Also  
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)