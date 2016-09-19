---
title: "TemplateData Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db17ec9b-bfdf-46b1-bbe7-5ccc140056e2
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TemplateData Element (Visual Studio Templates)
Categorizes the template and defines how it displays in either the **New Project** or the **Add New Item** dialog box.  
  
 <VSTemplate\>  
 <TemplateData\>  
  
## Syntax  
  
```  
<TemplateData>  
    <Name> ... </Name>  
    <Description> ... </Description>  
    <Icon> ... </Icon>  
    <ProjectType> ... </ProjectType>  
    ...  
</TemplateData>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Name](../vs140/Name-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Specifies the name of the template as it appears in either the **New Project** or the **Add New Item** dialog box.|  
|[Description](../vs140/Description-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Specifies the description of the template as it appears in either the **New Project** or the **Add New Item** dialog box.|  
|[Icon](../vs140/Icon-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Specifies the path and the filename of the image file that serves as the icon, which appears in either the **New Project** or the **Add New Item** dialog box, for the template.|  
|[ProjectType](../vs140/ProjectType-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Categorizes the project template so that it appears under the specified group in the **New Project** dialog box.|  
|[ProjectSubType](../vs140/ProjectSubType-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Classifies the project template so that it appears under the specified subcategory in the **New Project** dialog box.|  
|[TemplateID](../vs140/TemplateID-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the template ID.|  
|[TemplateGroupID](../vs140/TemplateGroupID-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the template group ID.|  
|[SortOrder](../vs140/SortOrder-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies a value that is used to arrange the template, among other templates in the same category, as it appears in either the **New Project** or **Add New Item** dialog box.|  
|[CreateNewFolder](../vs140/CreateNewFolder-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether a containing folder is created on instantiation of the project.|  
|[DefaultName](../vs140/DefaultName-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the name that the Visual Studio project system will generate for the project or item when it is created.|  
|[ProvideDefaultName](../vs140/ProvideDefaultName-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether the Visual Studio project system will generate the default name for a project or item when it is created.|  
|[PromptForSaveOnCreation](../vs140/PromptForSaveOnCreation-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether the project can be created as a temporary project.|  
|[EnableLocationBrowseButton](../vs140/EnableLocationBrowseButton-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether the **Browse** button is available in the **New Project** dialog box, so that users can easily modify the default directory where a new project is saved.|  
|[Hidden](../vs140/Hidden-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether the template appears in either the **New Project** or **Add New Item** dialog box.|  
|[NumberOfParentCategoriesToRollUp](../vs140/NumberOfParentCategoriesToRollUp--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the number of parent categories that will display the template in the **New Project** dialog box.|  
|[LocationFieldMRUPrefix](../vs140/LocationFieldMRUPrefix-Element--Visual-Studio-Templates-.md)|Optional element.|  
|[LocationField](../vs140/LocationField-Element--Visual-Studio-Project-Templates-.md)|Optional element.<br /><br /> Specifies whether or not the **Location** text box in the **New Project** dialog box is either enabled, disabled, or hidden for the project template.|  
|[RequiredFrameworkVersion](../vs140/RequiredFrameworkVersion-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Use this element if the template only supports a specific minimum version, and later versions if any, of the .NET Framework.|  
|[SupportsMasterPage](../vs140/SupportsMasterPage-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether the template supports a master page for web projects.|  
|[SupportsCodeSeparation](../vs140/SupportsCodeSeparation-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether the template supports code separation, or the code-behind page model, for web projects.|  
|[SupportsLanguageDropDown](../vs140/SupportsLanguageDropDown-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies whether the template is identical for multiple languages, and whether the **Language** option is available from the **New Project** dialog box.|  
|[TargetPlatformName](../vs140/TargetPlatformName-Element--Visual-Studio-Templates-.md)|Optional element.<br /><br /> Specifies the platform that the project template targets. This element specifies that a project template is used to create [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[VSTemplate](../vs140/VSTemplate-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Contains all the metadata for the project template, item template, or starter kit.|  
  
## Remarks  
 `TemplateData` is a required element.  
  
 If you do not include an optional element, the default value for that element is used.  
  
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