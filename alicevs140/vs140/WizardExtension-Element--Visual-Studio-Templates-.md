---
title: "WizardExtension Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d54b01c1-50f5-4b65-828c-686e2321cc8c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WizardExtension Element (Visual Studio Templates)
Contains the registration elements for customizing the template wizard.  
  
 <VSTemplate\>  
 ...  
 <WizardExtension\>  
  
## Syntax  
  
```  
<WizardExtension>  
    <Assembly>... </Assembly>  
    <FullClassName>... </FullClassName>  
</WizardExtension>  
```  
  
## Attributes and Elements  
 The following sections describe attribute, child elements, and parent elements.  
  
### Attributes  
 None.  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Assembly](../vs140/Assembly-Element--Visual-Studio-Template-Wizard-Extension-.md)|Required element.<br /><br /> Specifies the name or strong name of an assembly that appears in the global assembly cache. There must be at least one `Assembly` element in a `WizardExtension` element.|  
|[FullClassName](../vs140/FullClassName-Element--Visual-Studio-Template-Wizard-Extension-.md)|Required element.<br /><br /> The fully qualified name of the class that implements the `IWizard` interface. There must be at least one `FullClassName` element in a `WizardExtension` element.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[VSTemplate](../vs140/VSTemplate-Element--Visual-Studio-Templates-.md)|Contains all the metadata for the project template, item template, or starter kit.|  
  
## Remarks  
 `WizardExtension` is an optional child element of `VSTemplate`.  
  
## Example  
 The following example illustrates the metadata for the standard project template for a [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] Windows application.  
  
```  
<VSTemplate Version="3.0.0" Type="Item"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyTemplate</Name>  
        <Description>Template using IWizard extension</Description>  
        <Icon>TemplateIcon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
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
    <WizardExtension>  
        <Assembly>MyWizard, Version=1.0.3300.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a, Custom=null</Assembly>  
        <FullClassName>MyWizard.CustomWizard</FullClassName>  
    </WizardExtension>  
</VSTemplate>  
```  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [How to: Use Wizards with Project Templates](../Topic/How%20to:%20Use%20Wizards%20with%20Project%20Templates.md)