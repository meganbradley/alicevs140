---
title: "ProjectTemplateLink Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b0449111-8b48-45a1-a031-ea24b765e969
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ProjectTemplateLink Element (Visual Studio Templates)
Specifies the path to the .vstemplate file of one project in a multi-project template.  
  
 <VSTemplate\>  
 <TemplateContent\>  
 <ProjectCollection\>  
 <ProjectTemplateLink\>  
-or-  
<VSTemplate\>  
 <TemplateContent\>  
 <ProjectCollection\>  
 <SolutionFolder\>  
 <ProjectTemplateLink\>  
  
## Syntax  
  
```  
<ProjectTemplateLink ProjectName="Name">  
    PathToTemplateFile  
</ProjectTemplateLink>  
```  
  
## Attributes and Elements  
 The following sections describe attribute, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|`ProjectName`|Optional attribute.<br /><br /> Specifies the name for each individual project in a multi-project template. The **New Project** dialog box cannot assign names to individual projects.|  
|`CopyParameters`|Enables all the variables in the main group template to be copied to each of the linked templates.<br /><br /> The parameters in the linked templates have a prefix `"$ext_*$"`. For example, if in the parent group template the parameter `$projectname$` has a value **ExampleProject1**, when the linked template gets its turn to be executed, it acquires a parameter `$ext_projectname$`, which is a copy of the `$projectname$` parameter from the parent group template.<br /><br /> This enables linked templates to share some common parameters, which may be conveniently created only in the parent group template.<br /><br /> This attribute is optional, and it automatically defaults to `false` when it is not included.<br /><br /> Introduced in Visual Studio 2013 Update 2. To reference the correct product version, see [Referencing Assemblies Delivered in the Visual Studio 2013 SDK Update 2](assetId:///42b65c3e-e42b-4c39-98c8-bea285f25ffb).|  
  
### Child Elements  
 None.  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[ProjectCollection](../vs140/ProjectCollection-Element--Visual-Studio-Templates-.md)|Specifies the organization and contents of multi-project templates.|  
|[SolutionFolder](../vs140/SolutionFolder-Element--Visual-Studio-Templates-.md)|Groups projects in multi-project templates.|  
  
## Text Value  
 A text value is required.  
  
 This text specifies the path to the .vstemplate file of the template.  
  
## Remarks  
 Multi-project templates act as containers for two or more projects. The `ProjectTemplateLink` element is used to specify the location of the .vstemplate file for one of the projects in the template. The .vstemplate file of a multi-project template contains one `ProjectTemplateLink` element for each project in the template. For more information on multi-project templates, see [How to: Create Multi-Project Templates](../vs140/How-to--Create-Multi-Project-Templates.md).  
  
## Example  
 This example shows a simple multi-project root .vstemplate file. In this example, the template contains two projects, `My Windows Application` and `My Class Library`. The `ProjectName` attribute on the `ProjectTemplateLink` element sets the name for [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] to assign this project. If the `ProjectName` attribute does not exist, the name of the .vstemplate file is used as the project name.  
  
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
            <ProjectTemplateLink ProjectName="My Windows Application">  
                WindowsApp\MyTemplate.vstemplate  
            </ProjectTemplateLink>  
            <ProjectTemplateLink ProjectName="My Class Library" CopyParameters="true">  
                ClassLib\MyTemplate.vstemplate  
            </ProjectTemplateLink>  
        </ProjectCollection>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [How to: Create Multi-Project Templates](../vs140/How-to--Create-Multi-Project-Templates.md)