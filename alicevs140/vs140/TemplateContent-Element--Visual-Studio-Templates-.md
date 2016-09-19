---
title: "TemplateContent Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90ae401c-b294-49ac-98da-e0d274f5bebb
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TemplateContent Element (Visual Studio Templates)
Specifies the contents of the template.  
  
 <VSTemplate\>  
 <TemplateContent\>  
  
## Syntax  
  
```  
<TemplateContent>  
    ...  
</TemplateContent>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|[BuildOnLoad](../vs140/BuildProjectOnLoad--Visual-Studio-Templates-.md)|Specifies whether to build the solution when a project is created from the template.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[ProjectCollection](../vs140/ProjectCollection-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the organization and contents of multi-project templates.|  
|[Project](../vs140/Project-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies files or directories to add to the project.|  
|[References](../vs140/References-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the assembly references required for an item template.|  
|[ProjectItem](../vs140/ProjectItem-Element--Visual-Studio-Item-Templates-.md)|Optional element.<br /><br /> Specifies a file contained in the template.|  
|[CustomParameters](../vs140/CustomParameters-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies any custom parameters that are to be used when a project or item  is created from the template.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[VSTemplate](../vs140/VSTemplate-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Contains all the metadata for the project template, item template, or starter kit.|  
  
## Remarks  
 `TemplateContent` is a required element.  
  
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