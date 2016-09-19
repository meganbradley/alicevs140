---
title: "Wizard Support for Nested Projects"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1b496acc-b326-4cdb-bb48-e3b5c6f12e05
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Wizard Support for Nested Projects
The IDE runs two wizards that the parent project for nested projects can implement: the **New Project** wizard and the **Add Item** wizard.  
  
 If a user starts the **New Project** wizard by selecting **Add Project** and clicking **New Project** on the File menu or by selecting **Add** and right-clicking **New Project** in Solution Explorer, the IDE runs the **AddProject** command and the parent project's implementation of the **AddProject** command either returns a template project file, or a wizard (.vsz) file that has a set of context parameters.  
  
 Similarly, a parent project's implementation of **AddItem** wizards returns a .vsz file that has a different set of context parameters.  
  
 For more information about wizards, see [Wizard (.Vsz) File](../vs140/Wizard--.Vsz--File.md), [Context Parameters](../Topic/Context%20Parameters.md) and [Registering Project and Item Templates](../vs140/Registering-Project-and-Item-Templates.md).  
  
## See Also  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy?qualifyHint=False>   
 [Nesting Projects](../vs140/Nesting-Projects.md)