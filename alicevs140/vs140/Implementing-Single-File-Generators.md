---
title: "Implementing Single-File Generators"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fe9ef6b6-4690-4c2c-872c-301c980d17fe
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Implementing Single-File Generators
A custom tool — sometimes referred to as a single file generator — can be used to extend the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] and [!INCLUDE[csprcs](../vs140/includes/csprcs_md.md)] project systems in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. A custom tool is a COM component that implements the <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator?qualifyHint=False> interface. Using this interface, a custom tool transforms a single input file into a single output file. The result of the transformation may be source code, or any other output that is useful. Two examples of custom tool-generated code files are code generated in response to changes in a visual designer and files generated using Web Services Description Language (WSDL).  
  
 When a custom tool is loaded, or the input file is saved, the project system calls the <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator.Generate?qualifyHint=False> method, and passes a reference to a <xref:Microsoft.VisualStudio.Shell.Interop.IVsGeneratorProgress?qualifyHint=False> callback interface, whereby the tool can report its progress to the user.  
  
 The output file that the custom tool generates is added to the project with a dependency on the input file. The project system automatically determines the name of the output file, based on the string returned by the custom tool's implementation of <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator.DefaultExtension?qualifyHint=False>.  
  
 A custom tool must implement the <xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGenerator?qualifyHint=False> interface. Optionally, custom tools support the <xref:Microsoft.VisualStudio.OLE.Interop.IObjectWithSite?qualifyHint=False> interface to retrieve information from sources other than the input file. In any case, before you can use a custom tool, you must register it with the system or in the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] local registry. For more information on registering custom tools, see [Registering Custom Tools](../Topic/Registering%20Single%20File%20Generators.md).  
  
## See Also  
 [Determining the Default Namespace of a Project](../Topic/Determining%20the%20Default%20Namespace%20of%20a%20Project.md)   
 [Exposing Types to Visual Designers](../Topic/Exposing%20Types%20to%20Visual%20Designers.md)