---
title: "ProjectType Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ccf9d83f-c7f3-49c7-a31f-e1f22bec004c
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ProjectType Element (Visual Studio Templates)
Categorizes the project template so that it appears under the specified group in the **New Project** or **Add New Item** dialog box.  
  
> [!WARNING]
>  Project templates are supported for C++ starting in Visual Studio 2012. They are not supported for C++ in Visual Studio 2010 and earlier versions.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <ProjectType\>  
  
## Syntax  
  
```  
<ProjectType> CSharp/VisualBasic/VC/Web </ProjectType>  
```  
  
## Attributes and Elements  
 The following sections describe attribute, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[TemplateData](../vs140/TemplateData-Element--Visual-Studio-Templates-.md)|Categorizes the template and defines how it displays in either the **New Project** or the **Add New Item** dialog box.|  
  
## Text Value  
 A text value is required.  
  
 This value specifies the type of project the template will create, and must contain one of the following values:  
  
-   `CSharp`: Specifies that the template creates a [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] project or item.  
  
-   `VisualBasic`: Specifies that the template creates a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] project or item.  
  
-   `Web`: Specifies that the template creates a Web project or item. If the `ProjectType` element contains this value, the language of the project or item is defined in the [ProjectSubType Element (Visual Studio Templates)](../vs140/ProjectSubType-Element--Visual-Studio-Templates-.md).  
  
## Remarks  
 `ProjectType` is a required child element of `TemplateData`.  
  
 The value of the `ProjectType` element specifies where the template is located in the **New Project** or **Add New Item** dialog box. For example, a template with a `ProjectType` value of `CSharp` appears under the **Visual C#** node in the **New Project** dialog box.  
  
 A template subtype can be specified by using the [ProjectSubType](../vs140/ProjectSubType-Element--Visual-Studio-Templates-.md) element.  
  
## Example  
 The following example shows the metadata for a project template for a [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] application.  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic starter kit</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <Project File="MyStarterKit.csproj">  
            <ProjectItem>Form1.cs<ProjectItem>  
            <ProjectItem>Form1.Designer.cs</ProjectItem>  
            <ProjectItem>Program.cs</ProjectItem>  
            <ProjectItem>Properties\AssemblyInfo.cs</ProjectItem>  
            <ProjectItem>Properties\Resources.resx</ProjectItem>  
            <ProjectItem>Properties\Resources.Designer.cs</ProjectItem>  
            <ProjectItem>Properties\Settings.settings</ProjectItem>  
            <ProjectItem>Properties\Settings.Designer.cs</ProjectItem>  
        </Project>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [ProjectSubType Element (Visual Studio Templates)](../vs140/ProjectSubType-Element--Visual-Studio-Templates-.md)