---
title: "Item Element (MSBuild)"
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
ms.assetid: dcef5f91-0613-4bfc-8ee9-d7004bb6d3a9
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Item Element (MSBuild)
Contains a user-defined item and its metadata. Every item that is used in a [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] project must be specified as a child of an `ItemGroup` element.  
  
 <Project\>  
 <ItemGroup\>  
 <Item\>  
  
## Syntax  
  
```  
<Item Include="*.cs"  
        Exclude="MyFile.cs"  
        Remove="RemoveFile.cs"  
        Condition="'String A'=='String B'" >  
    <ItemMetadata1>...</ItemMetadata1>  
    <ItemMetadata2>...</ItemMetadata2>  
</Item>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Include`|Required attribute.<br /><br /> The file or wildcard to include in the list of items.|  
|`Exclude`|Optional attribute.<br /><br /> The file or wildcard to exclude from the list of items.|  
|`Condition`|Optional attribute.<br /><br /> The condition to be evaluated. For more information, see [MSBuild Conditions](../vs140/MSBuild-Conditions.md).|  
|`Remove`|Optional attribute.<br /><br /> The file or wildcard to remove from the list of items.<br /><br /> This attribute is valid only if it's specified for an item in an `ItemGroup` that's in a `Target`.|  
|`KeepMetadata`|Optional attribute.<br /><br /> The metadata for the source items to add to the target items. Only the metadata whose names are specified in the semicolon-delimited list are transferred from a source item to a target item. For more information, see [MSBuild Items](../vs140/MSBuild-Items.md).<br /><br /> This attribute is valid only if it's specified for an item in an `ItemGroup` that's in a `Target`.|  
|`RemoveMetadata`|Optional attribute.<br /><br /> The metadata for the source items to not transfer to the target items. All metadata is transferred from a source item to a target item except metadata whose names are contained in the semicolon-delimited list of names. For more information, see [MSBuild Items](../vs140/MSBuild-Items.md).<br /><br /> This attribute is valid only if it's specified for an item in an `ItemGroup` that's in a `Target`.|  
|`KeepDuplicates`|Optional attribute.<br /><br /> Specifies whether an item should be added to the target group if it's an exact duplicate of an existing item. If the source and target item have the same `Include` value but different metadata, the item is added even if `KeepDuplicates` is set to `false`. For more information, see [MSBuild Items](../vs140/MSBuild-Items.md).<br /><br /> This attribute is valid only if it's specified for an item in an `ItemGroup` that's in a `Target`.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[ItemMetadata](../vs140/ItemMetadata-Element--MSBuild-.md)|A user-defined item metadata key, which contains the item metadata value. There may be zero or more `ItemMetadata` elements in an item.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[ItemGroup](../vs140/ItemGroup-Element--MSBuild-.md)|Grouping element for items.|  
  
## Remarks  
 `Item` elements define inputs into the build system, and are grouped into item collections based on their user-defined collection names. These item collections can be used as parameters for [tasks](../Topic/MSBuild%20Tasks.md), which use the individual items in the collections to perform the steps of the build process. For more information, see [MSBuild Items](../vs140/MSBuild-Items.md).  
  
 Using the notation `@(`*myType*`)` enables a collection of items of type *myType* to be expanded into a semicolon-delimited list of strings, and passed to a parameter. If the parameter is of type `string`, then the value of the parameter is the list of elements, separated by semicolons. If the parameter is an array of strings (`string[]`), then each element is inserted into the array based on the location of the semicolons. If the task parameter is of type <xref:Microsoft.Build.Framework.ITaskItem?qualifyHint=False>`[]`, then the value is the contents of the item collection together with any metadata attached. To delimit each item by using a character other than a semicolon, use the syntax `@(`*myType*`, '`*separator*`')`.  
  
 The [!INCLUDE[vstecmsbuild](../vs140/includes/vstecmsbuild_md.md)] engine can evaluate wildcards such as `*` and `?` and recursive wildcards such as `/**/*.cs`. For more information, see [MSBuild Items](../vs140/MSBuild-Items.md).  
  
## Example  
 The following code example shows how to declare two items of type `CSFile`. The second declared item contains metadata that has `MyMetadata` set to `HelloWorld`.  
  
```  
<ItemGroup>  
    <CSFile Include="engine.cs; form.cs" />  
    <CSFile Include="main.cs" >  
        <MyMetadata>HelloWorld</MyMetadata>  
    </CSFile>  
</ItemGroup>  
```  
  
## See Also  
 [MSBuild Items](../vs140/MSBuild-Items.md)   
 [MSBuild Properties](../Topic/MSBuild%20Properties.md)   
 [MSBuild Project File Schema Reference](../vs140/MSBuild-Project-File-Schema-Reference.md)