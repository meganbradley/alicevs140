---
title: "ProvideDefaultName Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b0e7b20-fd6b-42e2-81d0-e5100cea0528
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ProvideDefaultName Element (Visual Studio Templates)
Specifies whether the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] project system will generate a default name for the template in the **Add New Item** or **New Project** dialog box.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <ProvideDefaultName\>  
  
## Syntax  
  
```  
<ProvideDefaultName> true/false </ProvideDefaultName>  
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
  
 The text must be either `true` or `false`, indicating whether or not to generate a default name for the template in the **Add New Item** or **New Project** dialog box.  
  
## Remarks  
 `ProvideDefaultName` is an optional element. The default value is `true`.  
  
 If the `ProvideDefaultName` element is `false`, the **Name** boxes of the **Add New Item** and **New Project** dialog boxes contain the value `<Enter_name>`.  
  
 Use the [DefaultName](../vs140/DefaultName-Element--Visual-Studio-Templates-.md) element to specify the default name of the project or item in the **Add New Item** and **New Project** dialog boxes.  
  
## Example  
 The following code example sets the `ProvideDefaultName` element to `false`.  
  
```  
<VSTemplate Type="Item" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyClass</Name>  
        <Description>My custom C# class.</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <ProvideDefaultName>false</ProvideDefaultName>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectItem>MyClass.cs</ProjectItem>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)