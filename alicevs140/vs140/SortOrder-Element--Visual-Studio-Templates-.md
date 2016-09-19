---
title: "SortOrder Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 151932c1-f08a-4f78-a8d0-bd2f32211a9c
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SortOrder Element (Visual Studio Templates)
Specifies a value that is used to arrange the template, among other templates in the same category, as it appears in either the **New Project** or **Add New Item** dialog box.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <SortOrder\>  
  
## Syntax  
  
```  
<SortOrder> ... </SortOrder>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[TemplateData](../vs140/TemplateData-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Categorizes the template and defines how it displays in either the **New Project** or the **Add New Item** dialog box.|  
  
## Text Value  
 A text value is required.  
  
 An `integer` that represents the sort order value.  
  
## Remarks  
 `SortOrder` is an optional element. The default value is 100, and all values must be multiples of 10.  
  
 The `SortOrder` element is ignored for user-created templates. All user-created templates are sorted alphabetically.  
  
 Templates that have low sort order values appear in either the **New Project** or **New Add Item** dialog box before templates that have high sort order values.  
  
## Example  
 The following example illustrates the metadata for a standard [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] class template.  
  
```  
<VSTemplate Type="Item" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyClass</Name>  
        <Description>My custom C# class template.</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <SortOrder>290</SortOrder>  
        <DefaultName>MyClass</DefaultName>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectItem>MyClass.cs</ProjectItem>  
    </TemplateContent>  
</VSTemplate>  
```  
  
 In this example, the `SortOrder` element is relatively high. It is likely that other [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] item templates will have a `SortOrder` value lower than `290` and will appear before this template in the **New Item** dialog box.  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)