---
title: "PropertyGroup Element (MSBuild)"
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
ms.assetid: ff1e6c68-b9a1-4263-a1ce-dc3b829a64d4
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PropertyGroup Element (MSBuild)
Contains a set of user-defined [Property](../vs140/Property-Element--MSBuild-.md) elements. Every `Property` element used in an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project must be a child of a `PropertyGroup` element.  
  
 <Project\>  
 <PropertyGroup\>  
  
## Syntax  
  
```  
<PropertyGroup Condition="'String A' == 'String B'">  
    <Property1>...</Property1>  
    <Property2>...</Property2>  
</PropertyGroup>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|Condition|Optional attribute.<br /><br /> Condition to be evaluated. For more information, see [MSBuild Conditions](../vs140/MSBuild-Conditions.md).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Property](../vs140/Property-Element--MSBuild-.md)|Optional element.<br /><br /> A user defined property name, which contains the property value. There may be zero or more *Property* elements in a `PropertyGroup` element.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Project](../vs140/Project-Element--MSBuild-.md)|Required root element of an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project file.|  
  
## Example  
 The following code example shows how to set properties based on a condition. In this example, if the value of the `CompileConfig` property is `DEBUG`, the `Optimization`, `Obfuscate`, and `OutputPath` properties inside of the `PropertyGroup` element are set.  
  
```  
<PropertyGroup Condition="'$(CompileConfig)' == 'DEBUG'" >  
    <Optimization>false</Optimization>  
    <Obfuscate>false</Obfuscate>  
    <OutputPath>$(OutputPath)\debug</OutputPath>  
</PropertyGroup>  
```  
  
## See Also  
 [MSBuild Project File Schema Reference](../vs140/MSBuild-Project-File-Schema-Reference.md)   
 [MSBuild Properties](../Topic/MSBuild%20Properties.md)