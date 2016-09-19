---
title: "Generating Code from a Domain-Specific Language"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e3706cc9-2afd-456a-a879-68425a248ebc
caps.latest.revision: 15
---
# Generating Code from a Domain-Specific Language
Microsoft [!INCLUDE[dsl](../vs140/includes/dsl_md.md)] provides a powerful way to generate code, documents, configuration files and other artifacts from data represented in models. Using [!INCLUDE[dsl](../vs140/includes/dsl_md.md)], you can create a set of classes that represent your data, and you can write your text templates in classes whose names and properties reflect that data.  
  
 For example, Fabrikam has an XML file of customer names and e-mail addresses. Their developers create a model in which Customer is a class, with properties name and e-mail. They write several text templates to process the data, including this fragment which produces a table of all the customers as part of an HTML page:  
  
```  
<table>  
<# foreach (Customer c in ContactList) {  #>  
  <tr><td> <#= c.FullName #> </td>   
      <td> <#= c.EmailAddress #> </td> </tr>  
<# } #>  </table>  
```  
  
 When the customer database is processed, the XML file is read into the model store. A *directive processor*, created by using [!INCLUDE[dsl](../vs140/includes/dsl_md.md)], makes the Customer class available to the code in the text template. Many text templates can be run against the same store.  
  
 Text templates are essential to [!INCLUDE[dsl](../vs140/includes/dsl_md.md)]. They are used to generate the source code for the elements of the domain model as well as for the VSPackage and the controls that are used to integrate the tools with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 This section discusses some of the ways to create, modify, and debug text templates used in [!INCLUDE[dsl](../vs140/includes/dsl_md.md)].  
  
## In This Section  
 [Accessing Models from Text Templates](../Topic/Accessing%20Models%20from%20Text%20Templates.md)  
  
 Provides basic information about referring to domain-specific language in text templates.  
  
 [Walkthrough: Debugging a Text Template that Accesses a Model](../vs140/Walkthrough--Debugging-a-Text-Template-that-Accesses-a-Model.md)  
  
 Describes how to do troubleshooting and debugging on a text template that refers to a domain-specific language.  
  
 [Walkthrough: Connecting a Host to a Generated Directive Processor](../vs140/Walkthrough--Connecting-a-Host-to-a-Generated-Directive-Processor.md)  
  
 Describes how to connect a custom host to a generated directive processor.  
  
 [The DslTextTransform Command](../vs140/The-DslTextTransform-Command.md)  
  
 Describes the command file that executes the TextTransform executable on the command line for text templates that reference domain-specific languages.  
  
## Reference  
 [Text Template Structure](../vs140/Writing-a-T4-Text-Template.md)  
  
 Provides the syntax of text template directives and control blocks.  
  
## Related Sections  
 [Code Generation in a Visual Studio project](../vs140/Design-Time-Code-Generation-by-using-T4-Text-Templates.md)  
  
 Explains the text template transformation process.  
  
 [Code Generation in a Build Process](../Topic/Code%20Generation%20in%20a%20Build%20Process.md)  
  
 Read this topic if you are generating files from a DSL on a build server.