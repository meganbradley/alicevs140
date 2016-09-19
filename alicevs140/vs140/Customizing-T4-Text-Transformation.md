---
title: "Customizing T4 Text Transformation"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 62cd9a3c-a6e1-4b29-93f5-f2a0cf47dc92
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Customizing T4 Text Transformation
Text templates are a feature of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] that allow you to generate program code or other text files through a transformation process. Using [!INCLUDE[vssdk_current_short](../vs140/includes/vssdk_current_short_md.md)], you can extend the default template transformation process by customizing the text template directive processor or the text template host.  
  
## In This Section  
 [The Text Template Transformation Process](../vs140/The-Text-Template-Transformation-Process.md)  
 Describes how text transformation works, and explains the role of the template host and the directive processors.  
  
 [Creating Custom Text Template Directive Processors](../Topic/Creating%20Custom%20T4%20Text%20Template%20Directive%20Processors.md)  
 The directive processor deals with directives in your template, such as `<#@template#>.` It runs during the compilation of the template, and can load assemblies and other resources. It can also insert code that will load resources at runtime. By defining your own directive processor, you can reduce the complexity of your templates.  
  
 [Invoking Text Transformation in a Visual Studio Extension](../Topic/Invoking%20Text%20Transformation%20in%20a%20VS%20Extension.md)  
 If you are writing a [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Extension such as a menu command or event handler, your extension can use the Text Templating Service to transform any text template. You can pass parameter data into the template by using the Session object, and get the values from within the template by using the `<#@parameter#>` directive.  
  
 [Creating Custom Text Template Hosts](../Topic/Processing%20Text%20Templates%20by%20using%20a%20Custom%20Host.md)  
 When the code of the text template executes, the host provides access to external files and the state of the application. For example, the host that runs text transformations in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] can provide access to solution explorer. It also displays errors in the error message window. If you want to run text transformations in a different context, you can define your own host that provides access to the services available in that context.  
  
 If you are writing a [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Extension, consider using the existing text transformation service instead of writing your own host. For more information, see [Invoking Text Transformation in a Visual Studio Extension](../Topic/Invoking%20Text%20Transformation%20in%20a%20VS%20Extension.md).  
  
## Reference  
 [Text Template Structure](../vs140/Writing-a-T4-Text-Template.md)  
  
 Provides the syntax of text template directives and control blocks.