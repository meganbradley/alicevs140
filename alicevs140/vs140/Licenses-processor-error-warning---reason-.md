---
title: "Licenses processor error-warning: &lt;reason&gt;"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Licenses processor error/warning: &lt;reason&gt;
ms.assetid: 85750198-7bd3-4936-b1eb-954dcc3ff573
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Licenses processor error-warning: &lt;reason&gt;
An error or warning message is displayed if a tool returns an error or a warning while processing a .licx file. As part of the build process, the project system transforms the Licenses.licx file (if present) into a binary file understood by the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] license manager. This transformation is done using in-process tools.  
  
 The most likely cause of such an error or warning is a bad .licx file. A .licx file can become corrupt if the file has been edited outside of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] or within [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] using a text editor.  
  
 These files are normally managed by the Windows Forms and Web Forms Designers.  
  
### To correct this error  
  
1.  Fix the format of the .licx file.  
  
     An error means that the binary file has not been generated, and that the build process will fail. Warnings are for informational purposes only.  
  
## See Also  
 [File Types and File Extensions in Visual Basic and Visual C#](assetId:///f793852c-da06-4d52-a826-65f635844772)