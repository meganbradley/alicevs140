---
title: "UpdateManifest Task"
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
ms.assetid: 1291fd33-b89e-4e15-8fb1-69f9625cf2d2
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UpdateManifest Task
Updates selected properties in a manifest and resigns.  
  
## Parameters  
 The following table describes the parameters of the `UpdateManifest` task.  
  
|Parameter|Description|  
|---------------|-----------------|  
|`ApplicationManifest`|Required <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False> parameter.<br /><br /> Specifies the application manifest.|  
|`ApplicationPath`|Required `String` parameter.<br /><br /> Specifies the path of the application manifest.|  
|`InputManifest`|Required <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False> parameter.<br /><br /> Specifies the manifest to update.|  
|`OutputManifest`|Optional <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False> output parameter.<br /><br /> Specifies the manifest that contains updated properties.|  
  
## Remarks  
 In addition to having the parameters that are listed in the table, this task inherits parameters from the <xref:Microsoft.Build.Utilities.Task?qualifyHint=False> class. For a list of these additional parameters and their descriptions, see [Task Base Class](../Topic/Task%20Base%20Class.md).  
  
## See Also  
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)