---
title: "ItemGroup Element (MSBuild)"
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
ms.assetid: aac894e3-a9f1-4bbc-a796-6ef07001f35b
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ItemGroup Element (MSBuild)
Contains a set of user-defined [Item](../vs140/Item-Element--MSBuild-.md) elements. Every item used in a [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project must be specified as a child of an `ItemGroup` element.  
  
 <Project\>  
 <ItemGroup\>  
  
## Syntax  
  
```  
<ItemGroup Condition="'String A' == 'String B'">  
    <Item1>... </Item1>  
    <Item2>... </Item2>  
</ItemGroup>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Condition`|Optional attribute. Condition to be evaluated. For more information, see [MSBuild Conditions](../vs140/MSBuild-Conditions.md).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Item](../vs140/Item-Element--MSBuild-.md)|Defines the inputs for the build process. There may be zero or more `Item` elements in an `ItemGroup`.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Project](../vs140/Project-Element--MSBuild-.md)|Required root element of an [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project file.|  
|[Target](../vs140/Target-Element--MSBuild-.md)|Starting with .NET Framework 3.5, the `ItemGroup` element can appear inside a `Target` element. For more information, see [MSBuild Targets](../vs140/MSBuild-Targets.md).|  
  
## Remarks  
  
## Example  
 The following code example shows the user-defined item collections `Res` and `CodeFiles` declared inside of an `ItemGroup` element. Each of the items in the `Res` item collection contains a user-defined child [ItemMetadata](../vs140/ItemMetadata-Element--MSBuild-.md) element.  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemGroup>  
        <Res Include = "Strings.fr.resources" >  
            <Culture>fr</Culture>  
        </Res>  
        <Res Include = "Dialogs.fr.resources" >  
            <Culture>fr</Culture>  
        </Res>  
  
        <CodeFiles Include="**\*.cs" Exclude="**\generated\*.cs" />  
        <CodeFiles Include="..\..\Resources\Constants.cs" />  
    </ItemGroup>  
...  
</Project>  
```  
  
## See Also  
 [MSBuild File Format](../vs140/MSBuild-Project-File-Schema-Reference.md)   
 [MSBuild Items](../vs140/MSBuild-Items.md)   
 [Common MSBuild Project Items](../vs140/Common-MSBuild-Project-Items.md)