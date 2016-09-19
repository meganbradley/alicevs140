---
title: "LocationField Element (Visual Studio Project Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6aaaa155-6ce0-4f7f-aa50-8d63d7a7c992
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# LocationField Element (Visual Studio Project Templates)
Specifies whether or not the **Location** text box in the **New Project** dialog box is enabled, disabled, or hidden for the project template.  
  
 <VSTemplate\>  
 <TemplateData\>  
 <LocationField\>  
  
## Syntax  
  
```  
<LocationField> Enabled/Disabled/Hidden </LocationField>  
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
|[TemplateData](../vs140/TemplateData-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Categorizes the template and defines how it displays in either the **New Project**.|  
  
## Text Value  
 A text value is required.  
  
 Valid text values are:  
  
-   `Enabled`, which specifies that the **Location** box of the **New Project** dialog box is enabled.  
  
-   `Disabled`, which specifies that the **Location** box of the **New Project** dialog box is disabled.  
  
-   `Hidden`, which specifies that the **Location** box of the **New Project** dialog box is hidden.  
  
## Remarks  
 The default value is `Enabled`.  
  
 The **Location** text box in the **New Project** dialog box enables users to change the default directory in which new projects are saved.  
  
 The value specified in the `Location` element is only honored by the dialog box if the underlying project system supports it.  
  
## Example  
 The following example illustrates the metadata for a [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] template.  
  
```  
<VSTemplate Type="Project" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>My template</Name>  
        <Description>A basic template</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <LocationField>Disabled</LocationField>  
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