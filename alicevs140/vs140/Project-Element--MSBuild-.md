---
title: "Project Element (MSBuild)"
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
ms.assetid: d1cda56a-dbef-4109-9201-39e962e3f653
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Element (MSBuild)
Required root element of an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project file.  
  
## Syntax  
  
```  
<Project InitialTargets="TargetA;TargetB"  
         DefaultTargets="TargetC;TargetD"  
         TreatAsLocalProperty="PropertyA;PropertyB"  
         ToolsVersion=<version number>  
         xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <Choose>... </Choose>  
    <PropertyGroup>... </PropertyGroup>  
    <ItemGroup>... </ItemGroup>  
    <Target>... </Target>  
    <UsingTask.../>  
    <ProjectExtensions>... </ProjectExtensions>  
    <Import... />  
</Project>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`DefaultTargets`|Optional attribute.<br /><br /> The default target or targets to be the entry point of the build if no target has been specified. Multiple targets are semi-colon (;) delimited.<br /><br /> If no default target is specified in either the `DefaultTargets` attribute or the [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] command line, the engine executes the first target in the project file after the [Import](../vs140/Import-Element--MSBuild-.md) elements have been evaluated.|  
|`InitialTargets`|Optional attribute.<br /><br /> The initial target or targets to be run before the targets specified in the `DefaultTargets` attribute or on the command line. Multiple targets are semi-colon (;) delimited.|  
|`ToolsVersion`|Optional attribute.<br /><br /> The version of the toolset MSBuild uses to determine the values for $(MSBuildBinPath) and $(MSBuildToolsPath).|  
|`TreatAsLocalProperty`|Optional attribute.<br /><br /> Property names that won't be considered to be global. This attribute prevents specific command-line properties from overriding property values that are set in a project or targets file and all subsequent imports. Multiple properties are semi-colon (;) delimited.<br /><br /> Normally, global properties override property values that are set in the project or targets file. If the property is listed in the `TreatAsLocalProperty` value, the global property value doesn't override property values that are set in that file and any subsequent imports. For more information, see [How to: Build the Same Source Files with Different Options](../vs140/How-to--Build-the-Same-Source-Files-with-Different-Options.md). **Note:**  You set global properties  at a command prompt by using the **/property** (or **/p**) switch. You can also set or modify global properties for child projects in a multi-project build by using the `Properties` attribute of the MSBuild task. For more information, see [MSBuild Task](../Topic/MSBuild%20Task.md).|  
|`Xmlns`|Required attribute.<br /><br /> The `xmlns` attribute must have the value of "http://schemas.microsoft.com/developer/msbuild/2003".|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Choose](../vs140/Choose-Element--MSBuild-.md)|Optional element.<br /><br /> Evaluates child elements to select one set of `ItemGroup` elements and/or `PropertyGroup` elements to evaluate.|  
|[Import](../vs140/Import-Element--MSBuild-.md)|Optional element.<br /><br /> Enables a project file to import another project file. There may be zero or more `Import` elements in a project.|  
|[ItemGroup](../vs140/ItemGroup-Element--MSBuild-.md)|Optional element.<br /><br /> A grouping element for individual items. Items are specified by using the [Item](../vs140/Item-Element--MSBuild-.md) element. There may be zero or more `ItemGroup` elements in a project.|  
|[ProjectExtensions](../vs140/ProjectExtensions-Element--MSBuild-.md)|Optional element.<br /><br /> Provides a way to persist non-[!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] information in an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project file. There may be zero or one `ProjectExtensions` elements in a project.|  
|[PropertyGroup](../vs140/PropertyGroup-Element--MSBuild-.md)|Optional element.<br /><br /> A grouping element for individual properties. Properties are specified by using the [Property](../vs140/Property-Element--MSBuild-.md) element. There may be zero or more `PropertyGroup` elements in a project.|  
|[Target](../vs140/Target-Element--MSBuild-.md)|Optional element.<br /><br /> Contains a set of tasks for [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] to sequentially execute. Tasks are specified by using the [Task](../vs140/Task-Element--MSBuild-.md) element. There may be zero or more `Target` elements in a project.|  
|[UsingTask](../Topic/UsingTask%20Element%20\(MSBuild\).md)|Optional element.<br /><br /> Provides a way to register tasks in [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)]. There may be zero or more `UsingTask` elements in a project.|  
  
### Parent Elements  
 None.  
  
## See Also  
 [How To: Specify Which Target to Build First](../vs140/How-to--Specify-Which-Target-to-Build-First.md)   
 [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md)   
 [MSBuild File Format](../vs140/MSBuild-Project-File-Schema-Reference.md)   
 [MSBuild](../Topic/MSBuild.md)