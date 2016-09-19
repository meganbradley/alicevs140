---
title: "Output Element (MSBuild)"
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
ms.assetid: 34bc7cd1-efd3-4b57-b691-4584eeb6a0e9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Output Element (MSBuild)
Stores task output values in items and properties.  
  
 <Project\>  
 <Target\>  
 <Task\>  
 <Output\>  
  
## Syntax  
  
```  
<Output TaskParameter="Parameter"  
    PropertyName="PropertyName"   
    Condition = "'String A' == 'String B'" />  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`TaskParameter`|Required attribute.<br /><br /> The name of the task's output parameter.|  
|`PropertyName`|Either the `PropertyName` or `ItemName` attribute is required.<br /><br /> The property that receives the task's output parameter value. Your project can then reference the property with the `$(`*PropertyName*`)` syntax. This property name can either be a new property name or a name that is already defined in the project.<br /><br /> This attribute cannot be used if `ItemName` is also being used.|  
|`ItemName`|Either the `PropertyName` or `ItemName` attribute is required.<br /><br /> The item that receives the task's output parameter value. Your project can then reference the item with the `@(`*ItemName*`)` syntax. The item name can either be a new item name or a name that is already defined in the project.<br /><br /> This attribute cannot be used if `PropertyName` is also being used.|  
|`Condition`|Optional attribute.<br /><br /> Condition to be evaluated. For more information, see [MSBuild Conditions](../vs140/MSBuild-Conditions.md).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Task](../vs140/Task-Element--MSBuild-.md)|Creates and executes an instance of an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] task.|  
  
## Example  
 The following code example shows the `Csc` task being executed inside of a `Target` element. The items and properties passed to the task parameters are declared outside of the scope of this example. The value from the output parameter `OutputAssembly` is stored in the `FinalAssemblyName` item, and the value from the output parameter `BuildSucceeded` is stored in the `BuildWorked` property. For more information, see [MSBuild Tasks](../Topic/MSBuild%20Tasks.md).  
  
```  
<Target Name="Compile" DependsOnTargets="Resources">  
    <Csc  Sources="@(CSFile)"  
            TargetType="library"  
            Resources="@(CompiledResources)"  
            EmitDebugInformation="$(includeDebugInformation)"  
            References="@(Reference)"  
            DebugType="$(debuggingType)"  
            OutputAssembly="$(builtdir)\$(MSBuildProjectName).dll" >  
        <Output TaskParameter="OutputAssembly"  
                  ItemName="FinalAssemblyName" />  
        <Output TaskParameter="BuildSucceeded"  
                  PropertyName="BuildWorked" />  
    </Csc>  
</Target>  
```  
  
## See Also  
 [MSBuild Project File Schema Reference](../vs140/MSBuild-Project-File-Schema-Reference.md)   
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)