---
title: "FullClassName Element (Visual Studio Template Wizard Extension)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 651e1010-d529-4856-85ff-c77ceca5d2ed
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FullClassName Element (Visual Studio Template Wizard Extension)
The fully qualified name of the class that implements the `IWizard` interface.  
  
 <VSTemplate\>  
 <WizardExtension\>  
 ...  
 <FullClassName\>  
  
## Syntax  
  
```  
<FullClassName>ClassName</FullClassName>  
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
|[WizardExtension](../vs140/WizardExtension-Element--Visual-Studio-Templates-.md)|Contains the registration elements for customizing the template wizard.|  
  
## Text Value  
 A text value is required.  
  
 This text specifies the class that implements the `IWizard` interface. The specified class must exist in the assembly specified by the [Assembly](../vs140/Assembly-Element--Visual-Studio-Template-Wizard-Extension-.md) element.  
  
## Remarks  
 `FullClassName` is a required child element of `WizardExtension`.  
  
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