---
title: "AssignTargetPath Task"
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
ms.assetid: 0e830e31-3bcf-4259-b2a8-a5df49b92d51
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AssignTargetPath Task
This task accepts a list files and adds `<TargetPath>` attributes if they are not already specified.  
  
## Task Parameters  
 The following table describes the parameters of the `AssignTargetPath` task.  
  
|Parameter|Description|  
|---------------|-----------------|  
|`RootFolder`|Optional `string` input parameter.<br /><br /> Contains the path to the folder that contains the target links.|  
|`Files`|Optional <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False>`[]` input parameter.<br /><br /> Contains the incoming list of files.|  
|`AssignedFiles`|Optional<br /><br /> <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False> `[]` output parameter.<br /><br /> Contains the resulting list of files.|  
  
## Remarks  
 In addition to the parameters listed above, this task inherits parameters from the <xref:Microsoft.Build.Tasks.TaskExtension?qualifyHint=False> class, which itself inherits from the <xref:Microsoft.Build.Utilities.Task?qualifyHint=False> class. For a list of these additional parameters and their descriptions, see [TaskExtension Base Class](../Topic/TaskExtension%20Base%20Class.md).  
  
## Example  
 The following example executes the `AssignTargetPath` task to configure a project.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Target Name="MyProject">  
        <AssignTargetPath  
RootFolder="Resources"  
            Files="@(ResourceFiles)"  
            <Output TaskParameter="AssignedFiles"  
                ItemName="OutAssignedFiles"/>  
        </AssignTargetPath>  
    </Target>  
</Project>  
```  
  
## See Also  
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)