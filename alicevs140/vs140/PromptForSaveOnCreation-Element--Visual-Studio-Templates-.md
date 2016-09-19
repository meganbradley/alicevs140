---
title: "PromptForSaveOnCreation Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 75174674-0c3c-4b57-b2fd-6ea8e817b67d
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PromptForSaveOnCreation Element (Visual Studio Templates)
Specifies whether the user is prompted for a project save location via the **New Project** dialog box when creating a project. If this element is set to `true`, then the user is prompted for a save location; if `false`, then they are not prompted. (That is, a temporary project is created.)  
  
 <VSTemplate\>  
 <TemplateData\>  
 <PromptForSaveOnCreation\>  
  
## Syntax  
  
```  
<PromptForSaveOnCreation> true/false </PromptForSaveOnCreation>  
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
  
 The text must be either `true` or `false`, `true` indicating that the user will be prompted for a save location when creating a new project.  
  
## Remarks  
 `PromptForSaveOnCreation` is an optional element. The default value is `false`.  
  
 Temporary projects are projects that you can create and modify without saving the contents of that project on disk. For more information, see [NIB Temporary Projects](assetId:///9cf1944c-7045-44cc-8701-7b0eb4099f2b).  
  
## Example  
 The following example sets the value of `PromptForSaveOnCreation` equal to `false`, which specifies to allow the project to be created as a temporary project.  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic template</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <PromptForSaveOnCreation>false</PromptForSaveOnCreation>  
    </TemplateData>  
    <TemplateContent>  
        <Project File="MyTemplate.csproj">  
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