---
title: "MSBuild .Targets Files"
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
ms.assetid: f6d98eb4-d2fa-49b7-8e3c-bae1ca3cf596
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild .Targets Files
[!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] includes several .targets files that contain items, properties, targets, and tasks for common scenarios. These files are automatically imported into most [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] project files to simplify maintenance and readability.  
  
 Projects typically import one or more .targets files to define their build process. For example a [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] project created by [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] will import Microsoft.CSharp.targets which imports Microsoft.Common.targets. The [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] project itself will define the items and properties specific to that project, but the standard build rules for a [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] project are defined in the imported .targets files.  
  
 The `$(MSBuildToolsPath)` value specifies the path of these common .targets files. If the `ToolsVersion` is 4.0, the files are in the following location: `WindowsInstallationPath\Microsoft.NET\Framework\v4.0.30319\`  
  
> [!NOTE]
>  For information about how to create your own targets, see [MSBuild Targets](../vs140/MSBuild-Targets.md). For information about how to use the `Import` element to insert a project file into another project file, see [Import Element (MSBuild)](../vs140/Import-Element--MSBuild-.md) and [How to: Use the Same Target in Multiple Project Files](../vs140/How-to--Use-the-Same-Target-in-Multiple-Project-Files.md).  
  
## Common .Targets Files  
  
|.Targets file|Description|  
|-------------------|-----------------|  
|Microsoft.Common.targets|Defines the steps in the standard build process for [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] and [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] projects.<br /><br /> Imported by the Microsoft.CSharp.targets and Microsoft.VisualBasic.targets files, which include the following statement: `<Import Project="Microsoft.Common.targets" />`|  
|Microsoft.CSharp.targets|Defines the steps in the standard build process for Visual C# projects.<br /><br /> Imported by Visual C# project files (.csproj), which include the following statement: `<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />`|  
|Microsoft.VisualBasic.targets|Defines the steps in the standard build process for Visual Basic projects.<br /><br /> Imported by Visual Basic project files (.vbproj), which include the following statement: `<Import Project="$(MSBuildToolsPath)\Microsoft.VisualBasic.targets" />`|  
  
## See Also  
 [Import Element (MSBuild)](../vs140/Import-Element--MSBuild-.md)   
 [MSBuild Reference](../Topic/MSBuild%20Reference.md)   
 [MSBuild](../Topic/MSBuild.md)