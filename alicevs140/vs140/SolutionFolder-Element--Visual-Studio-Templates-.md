---
title: "SolutionFolder Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 963f0398-fb50-4d8e-879d-d48f8b7c6d80
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SolutionFolder Element (Visual Studio Templates)
Groups projects in multi-project templates.  
  
 <VSTemplate\>  
 <TemplateContent\>  
 <ProjectCollection\>  
 <SolutionFolder\>  
  
## Syntax  
  
```  
<SolutionFolder Name="DirectoryName">  
    ...  
</SolutionFolder>  
```  
  
## Attributes and Elements  
 The following sections describe attribute, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`Name`|Required attribute.<br /><br /> The name of the solution folder.|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[ProjectTemplateLink](../vs140/ProjectTemplateLink-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the path to the .vstemplate file of one project in a multi-project template.|  
|`SolutionFolder`|Optional element.<br /><br /> Groups projects in multi-project templates.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[ProjectCollection](../vs140/ProjectCollection-Element--Visual-Studio-Templates-.md)|Specifies the organization and contents of multi-project templates.|  
|`SolutionFolder`|Groups projects in multi-project templates.|  
  
## Remarks  
 Multi-project templates act as containers for two or more projects. The `SolutionFolder` element is used to organize the projects in the template into groups. The folders specified by `SolutionFolder` elements are created as solution folders in the project in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. For more information on multi-project templates, see [How to: Create Multi-Project Templates](../vs140/How-to--Create-Multi-Project-Templates.md).  
  
## Example  
 This example uses the `SolutionFolder` element to divide the multi-project template into two groups, `Math Classes` and `Graphics Classes`. The template contains four projects, two of which are placed in each solution folder.  
  
```  
<VSTemplate Version="3.0.0" Type="ProjectGroup"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>Multi-Project Template Sample</Name>  
        <Description>An example of a multi-project template</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>VisualBasic</ProjectType>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectCollection>  
            <SolutionFolder Name="Math Classes">  
                <ProjectTemplateLink ProjectName="MathClassLib1">  
                    MathClassLib1\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
                <ProjectTemplateLink ProjectName="MathClassLib2">  
                    MathClassLib2\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
            </SolutionFolder>  
            <SolutionFolder Name="Graphics Classes">  
                <ProjectTemplateLink ProjectName="GraphicsClassLib1">  
                    GraphicsClassLib1\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
                <ProjectTemplateLink ProjectName="GraphicsClassLib2">  
                    GraphicsClassLib2\MyTemplate.vstemplate  
                </ProjectTemplateLink>  
            </SolutionFolder>  
        </ProjectCollection>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [How to: Create Multi-Project Templates](../vs140/How-to--Create-Multi-Project-Templates.md)