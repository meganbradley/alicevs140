---
title: "WizardData Element (Visual Studio Templates)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d0403a16-5d07-4fe5-b474-19ae3d9fd3ab
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WizardData Element (Visual Studio Templates)
Specifies custom XML  
  
 <VSTemplate\>  
 <WizardData\>  
  
## Syntax  
  
```  
<WizardData>  
    <!-- XML to pass to the custom wizard extension -->  
    ...  
</WizardData>  
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
|[VSTemplate](../vs140/VSTemplate-Element--Visual-Studio-Templates-.md)|Required element.<br /><br /> Contains all the metadata for the project template, item template, or starter kit.|  
  
## Text Value  
 A text value is optional.  
  
 This text specifies the custom XML to pass to the custom wizard extension specified in the [WizardExtension](../vs140/WizardExtension-Element--Visual-Studio-Templates-.md) element.  
  
## Remarks  
 Any XML can be specified in this element. The XML will be passed as a parameter to the custom wizard extension, allowing the extension to use the contents of this element. No validation is done on this data.  
  
 The contents of the `WizardData` element are passed, unchanged, as a parameter inside the string dictionary of parameters in the `IWizard.RunStarted` method. The parameter is named $WizardData$.  
  
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
    <WizardData>  
        <!-- XML to pass to the custom wizard extension -->  
    </WizardData>  
</VSTemplate>  
```  
  
## See Also  
 [Visual Studio Template Schema Reference](../vs140/Visual-Studio-Template-Schema-Reference.md)   
 [Introduction to Visual Studio Templates](../vs140/Creating-Project-and-Item-Templates.md)   
 [WizardExtension Element (Visual Studio Templates)](../vs140/WizardExtension-Element--Visual-Studio-Templates-.md)   
 [How to: Use Wizards with Project Templates](../Topic/How%20to:%20Use%20Wizards%20with%20Project%20Templates.md)