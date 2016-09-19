---
title: "ItemMetadata Element (MSBuild)"
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
ms.assetid: e3db5122-202d-43a9-b2f4-3e0ec4ed3d08
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ItemMetadata Element (MSBuild)
Contains a user-defined item metadata key, which contains the item metadata value. An item may have any number of metadata key-value pairs.  
  
 <Project\>  
 <ItemGroup\>  
 <Item\>  
  
## Syntax  
  
```  
<ItemMetadataName> Item Metadata value</ItemMetadataName>  
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
|[Item](../vs140/Item-Element--MSBuild-.md)|A user-defined element that defines the inputs for the build process.|  
  
## Text Value  
 A text value is optional.  
  
 This text specifies the item metadata value, which can be either text or XML.  
  
## Remarks  
  
## Example  
 The following code example shows how to add `Culture` metadata with the value `fr` to the item `CSFile`.  
  
```  
<ItemGroup>  
    <CSFile Include="main.cs" >  
        <Culture>fr</Culture>  
    </CSFile>  
</ItemGroup>  
```  
  
## See Also  
 [MSBuild File Format](../vs140/MSBuild-Project-File-Schema-Reference.md)   
 [MSBuild Items](../vs140/MSBuild-Items.md)