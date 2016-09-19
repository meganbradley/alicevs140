---
title: "Task Element (MSBuild)"
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
ms.assetid: d82e2485-e5f0-4936-a357-745bacccc299
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Task Element (MSBuild)
Creates and executes an instance of an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] task. The element name is determined by the name of the task being created.  
  
 <Project\>  
 <Target\>  
  
## Syntax  
  
```  
<Task Parameter1="Value1"... ParameterN="ValueN"  
    ContinueOnError="WarnAndContinue/true/ErrorAndContinue/ErrorAndStop/false"  
    Condition="'String A' == 'String B'" >  
    <Output... />  
</Task>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Condition`|Optional attribute. Condition to be evaluated. For more information, see [MSBuild Conditions](../vs140/MSBuild-Conditions.md).|  
|`ContinueOnError`|Optional attribute. Can contain one of the following values:<br /><br /> -   **WarnAndContinue** or **true**. When a task fails, subsequent tasks in the [Target](../vs140/Target-Element--MSBuild-.md) element and the build continue to execute, and all errors from the task are treated as warnings.<br />-   **ErrorAndContinue**. When a task fails, subsequent tasks in the `Target` element and the build continue to execute, and all errors from the task are treated as errors.<br />-   **ErrorAndStop** or **false** (default). When a task fails, the remaining tasks in the `Target` element and the build aren't executed, and the entire `Target` element and the build is considered to have failed.<br /><br /> Versions of the .NET Framework before 4.5 supported only the `true` and `false` values.<br /><br /> For more information, see [How to: Ignore Errors in Tasks](../vs140/How-to--Ignore-Errors-in-Tasks.md).|  
|`Parameter`|Required if the task class contains one or more properties labeled with the `[Required]` attribute.<br /><br /> A user-defined task parameter that contains the parameter value as its value. There can be any number of parameters in the `Task` element, with each attribute mapping to a .NET property in the task class.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Output](../vs140/Output-Element--MSBuild-.md)|Stores outputs from the task in the project file. There may be zero or more `Output` elements in a task.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Target](../vs140/Target-Element--MSBuild-.md)|Container element for [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] tasks.|  
  
## Remarks  
 A `Task` element in an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project file creates an instance of a task, sets properties on it, and executes it. The `Output` element stores output parameters in properties or items to be used elsewhere in the project file.  
  
 If there are any [OnError](../vs140/OnError-Element--MSBuild-.md) elements in the parent `Target` element of a task, they will still be evaluated if the task fails and `ContinueOnError` has a value of `false`. For more information on tasks, see [MSBuild Tasks](../Topic/MSBuild%20Tasks.md).  
  
## Example  
 The following code example creates an instance of the [Csc task](../vs140/Csc-Task.md) class, sets six of the properties, and executes the task. After execution, the value of the `OutputAssembly` property of the object is placed into an item list named `FinalAssemblyName`.  
  
```  
<Target Name="Compile" DependsOnTarget="Resources" >  
    <Csc Sources="@(CSFile)"  
          TargetType="library"  
          Resources="@(CompiledResources)"  
          EmitDebugInformation="$(includeDebugInformation)"  
          References="@(Reference)"  
          DebugType="$(debuggingType)" >  
        <Output TaskParameter="OutputAssembly"  
                  ItemName="FinalAssemblyName" />  
    </Csc>  
</Target>  
```  
  
## See Also  
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)   
 [MSBuild Task Reference](../Topic/MSBuild%20Task%20Reference.md)   
 [MSBuild File Format](../vs140/MSBuild-Project-File-Schema-Reference.md)