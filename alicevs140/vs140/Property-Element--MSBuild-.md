---
title: "Property Element (MSBuild)"
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
ms.assetid: 69ab08ab-3e76-41dd-a01b-49aa1d2e0cac
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property Element (MSBuild)
Contains a user defined property name and value. Every property used in an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project must be specified as a child of a `PropertyGroup` element.  
  
 <Project\>  
 <PropertyGroup\>  
  
## Syntax  
  
```  
<Property Condition="'String A' == 'String B'">  
    Property Value  
</Property>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Condition`|Optional attribute.<br /><br /> Condition to be evaluated. For more information, see [MSBuild Conditions](../vs140/MSBuild-Conditions.md).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[PropertyGroup](../vs140/PropertyGroup-Element--MSBuild-.md)|Grouping element for properties.|  
  
## Text Value  
 A text value is optional.  
  
 This text specifies the property value and may contain XML.  
  
## Remarks  
 Property names are limited to ASCII chars only. Property values are referenced in the project by placing the property name between "`$(`" and "`)`". For example, `$(builddir)\classes` would resolve to "build\classes", if the `builddir` property had the value `build`. For more information on properties, see [MSBuild Properties](../Topic/MSBuild%20Properties.md).  
  
## Example  
 The following code sets the `Optimization` property to `false` and the `DefaultVersion` property to `1.0` if the `Version` property is empty.  
  
```  
<PropertyGroup>  
    <Optimization>false</Optimization>  
    <DefaultVersion Condition="'$(Version)' == ''" >1.0</DefaultVersion>  
</PropertyGroup>  
```  
  
## See Also  
 [MSBuild Properties](../Topic/MSBuild%20Properties.md)   
 [MSBuild File Format](../vs140/MSBuild-Project-File-Schema-Reference.md)