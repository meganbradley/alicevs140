---
title: "GetAssemblyIdentity Task"
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
ms.assetid: a977e072-37ad-4941-84a6-32a4483be55d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# GetAssemblyIdentity Task
Retrieves the assembly identities from the specified files and outputs the identity information.  
  
## Task Parameters  
 The following table describes the parameters of the `GetAssemblyIdentity` task.  
  
|Parameter|Description|  
|---------------|-----------------|  
|`Assemblies`|Optional <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False>`[]` output parameter.<br /><br /> Contains the retrieved assembly identities.|  
|`AssemblyFiles`|Required <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False>`[]` parameter.<br /><br /> Specifies the files to retrieve identities from.|  
  
## Remarks  
 The items output by the `Assemblies` parameter contain item metadata entries named `Version`, `PublicKeyToken`, and `Culture`.  
  
 In addition to the parameters listed above, this task inherits parameters from the <xref:Microsoft.Build.Tasks.TaskExtension?qualifyHint=False> class, which itself inherits from the <xref:Microsoft.Build.Utilities.Task?qualifyHint=False> class. For a list of these additional parameters and their descriptions, see [TaskExtension Base Class](../Topic/TaskExtension%20Base%20Class.md).  
  
## Example  
 The following example retrieves the identity of the files specified in the `MyAssemblies` item, and outputs them into the `MyAssemblyIdentities` item.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <MyAssemblies Include="File1.dll;File2.dll" />  
    </ItemGroup>  
  
    <Target Name="RetrieveIdentities>  
        <GetAssemblyIdentity  
            AssemblyFiles="@(MyAssemblies)"  
            <Output  
                TaskParameter="Assemblies"  
                ItemName="MyAssemblyIdentities"  
    </Target>  
  
</Project>  
```  
  
## See Also  
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)