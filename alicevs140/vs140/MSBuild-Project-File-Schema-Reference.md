---
title: "MSBuild Project File Schema Reference"
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
ms.assetid: d9a68146-1f43-4621-ac78-2c8c3f400936
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Project File Schema Reference
Provides a table of all the [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] XML Schema elements with their available attributes and child elements.  
  
 [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] uses project files to instruct the build engine what to build and how to build it. [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project files are XML files that adhere to the [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] XML schema. This section documents the XML schema definition (.xsd) file for [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)].  
  
## MSBuild XML Schema Elements  
 The following table lists all of the [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] XML schema elements along with their child elements and attributes.  
  
|Element|Child Elements|Attributes|  
|-------------|--------------------|----------------|  
|[Choose Element (MSBuild)](../vs140/Choose-Element--MSBuild-.md)|Otherwise<br /><br /> When|--|  
|[Import Element (MSBuild)](../vs140/Import-Element--MSBuild-.md)|--|Condition<br /><br /> Project|  
|[ImportGroup Element &#91;MSBuild&#93;](../vs140/ImportGroup-Element.md)|Import|Condition|  
|[Item Element (MSBuild)](../vs140/Item-Element--MSBuild-.md)|*ItemMetaData*|Condition<br /><br /> Exclude<br /><br /> Include<br /><br /> Remove|  
|[ItemDefinitionGroup Element (MSBuild)](../vs140/ItemDefinitionGroup-Element--MSBuild-.md)|*Item*|Condition|  
|[ItemGroup Element (MSBuild)](../vs140/ItemGroup-Element--MSBuild-.md)|*Item*|Condition|  
|[ItemMetaData Element (MSBuild)](../vs140/ItemMetadata-Element--MSBuild-.md)|*Item*|Condition|  
|[OnError Element (MSBuild)](../vs140/OnError-Element--MSBuild-.md)|--|Condition<br /><br /> ExecuteTargets|  
|[Otherwise Element (MSBuild)](../vs140/Otherwise-Element--MSBuild-.md)|Choose<br /><br /> ItemGroup<br /><br /> PropertyGroup|--|  
|[Output Element (MSBuild)](../vs140/Output-Element--MSBuild-.md)|--|Condition<br /><br /> ItemName<br /><br /> PropertyName<br /><br /> TaskParameter|  
|[Parameter Element &#91;MSBuild&#93;](../vs140/Parameter-Element.md)|--|Output<br /><br /> ParameterType<br /><br /> Required|  
|[ParameterGroup Element &#91;MSBuild&#93;](../vs140/ParameterGroup-Element.md)|*Parameter*|--|  
|[Project Element (MSBuild)](../vs140/Project-Element--MSBuild-.md)|Choose<br /><br /> Import<br /><br /> ItemGroup<br /><br /> ProjectExtensions<br /><br /> PropertyGroup<br /><br /> Target<br /><br /> UsingTask|DefaultTargets<br /><br /> InitialTargets<br /><br /> ToolsVersion<br /><br /> TreatAsLocalProperty<br /><br /> xmlns|  
|[ProjectExtensions Element (MSBuild)](../vs140/ProjectExtensions-Element--MSBuild-.md)|--|--|  
|[Property Element (MSBuild)](../vs140/Property-Element--MSBuild-.md)|--|Condition|  
|[PropertyGroup Element (MSBuild)](../vs140/PropertyGroup-Element--MSBuild-.md)|*Property*|Condition|  
|[Target Element (MSBuild)](../vs140/Target-Element--MSBuild-.md)|OnError<br /><br /> *Task*|AfterTargets<br /><br /> BeforeTargets<br /><br /> Condition<br /><br /> DependsOnTargets<br /><br /> Inputs<br /><br /> KeepDuplicateOutputs<br /><br /> Name<br /><br /> Outputs<br /><br /> Returns|  
|[Task Element (MSBuild)](../vs140/Task-Element--MSBuild-.md)|Output|Condition<br /><br /> ContinueOnError<br /><br /> *Parameter*|  
|[TaskBody Element (MSBuild)](../vs140/TaskBody-Element--MSBuild-.md)|*Data*|Evaluate|  
|[UsingTask Element (MSBuild)](../Topic/UsingTask%20Element%20\(MSBuild\).md)|ParameterGroup<br /><br /> TaskBody|AssemblyFile<br /><br /> AssemblyName<br /><br /> Condition<br /><br /> TaskFactory<br /><br /> TaskName|  
|[When Element (MSBuild)](../vs140/When-Element--MSBuild-.md)|Choose<br /><br /> ItemGroup<br /><br /> PropertyGroup|Condition|  
  
## See Also  
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)   
 [MSBuild Conditions](../vs140/MSBuild-Conditions.md)   
 [MSBuild Reference](../Topic/MSBuild%20Reference.md)   
 [MSBuild](../Topic/MSBuild.md)