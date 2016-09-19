---
title: "Legacy Language Service Features1"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
H1: Legacy Language Service Features
ms.assetid: a646e4f0-767d-4cd1-8e1a-9a2aa210a1b7
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Legacy Language Service Features1
A managed package framework (MPF) language service can support one or more [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] features, such as syntax highlighting, IntelliSense, and breakpoint validation. Each feature can be implemented independent of the others but all require a parser and a scanner except for syntax highlighting, which requires only a scanner.  
  
## In This Section  
 [Brace Matching (Managed Package Framework)](../Topic/Brace%20Matching%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support language pair matching, also known as brace matching.  
  
 [Commenting Blocks of Code (Managed Package Framework)](../vs140/Commenting-Code-in-a-Legacy-Language-Service.md)  
 Describes what is required to support commenting and uncommenting of selected code.  
  
 [Custom Document Properties (Managed Package Framework)](../Topic/Custom%20Document%20Properties%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support document properties that are embedded in a source file.  
  
 [Outlining (Managed Package Framework)](../Topic/Outlining%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support outlining through the implementation of hidden regions.  
  
 [Reformatting Code (Managed Package Framework)](../Topic/Reformatting%20Code%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support reformatting code.  
  
 [Supporting Code Snippets (Managed Package Framework)](../vs140/Support-for-Code-Snippets-in-a-Legacy-Language-Service.md)  
 Describes what is required to support code snippets, which are segments of code that are inserted and can be edited.  
  
 [Supporting IntelliSense Parameter Info (Managed Package Framework)](../Topic/Parameter%20Info%20in%20a%20Legacy%20Language%20Service2.md)  
 Describes what is required to support the IntelliSense Parameter Info operation for displaying a method signature as the method is typed.  
  
 [Supporting IntelliSense Quick Info (Managed Package Framework)](../Topic/Quick%20Info%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support the IntelliSense Quick Info operation for displaying information about an identifier.  
  
 [Supporting IntelliSense Member Completion (Managed Package Framework)](../Topic/Member%20Completion%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support the IntelliSense Member Completion operation for selecting a member of a namespace from a list.  
  
 [Supporting IntelliSense Complete Word (Managed Package Framework)](../Topic/Word%20Completion%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support the IntelliSense Complete Word operation for completing partially typed words.  
  
 [Supporting the Autos Window (Managed Package Framework)](../vs140/Support-for-the-Autos-Window-in-a-Legacy-Language-Service.md)  
 Describes what a language service can do to support the **Autos** window while you are debugging.  
  
 [Supporting the Navigation Bar](../vs140/Support-for-the-Navigation-Bar-in-a-Legacy-Language-Service.md)  
 Describes how to use the **Navigation bar** across the top of the editor view to provide quick navigation to any type or member in the file shown in that view..  
  
 [Syntax Highlighting (Managed Package Framework)](../Topic/Syntax%20Colorizing%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what is required to support syntax highlighting of source code.  
  
 [Validating Breakpoints (Managed Package Framework)](../Topic/Validating%20Breakpoints%20in%20a%20Legacy%20Language%20Service.md)  
 Describes what a language service can do to support validating breakpoints outside a debugger.  
  
## Related Sections  
 [The Language Service Parser and Scanner (Managed Package Framework)](../Topic/Legacy%20Language%20Service%20Parser%20and%20Scanner.md)  
 Describes the parser and scanner that are required to implement all the features of a language service that uses the managed package framework.  
  
 [Implementing a Language Service (Managed Package Framework)](../Topic/Implementing%20a%20Legacy%20Language%20Service2.md)  
 Describes what is required to implement a language service by using the MPF.  
  
 [Registering a Language Service (Managed Package Framework)](../vs140/Registering-a-Legacy-Language-Service1.md)  
 Describes the steps that are required to register an MPF-based language service with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Using IntelliSense](../vs140/Using-IntelliSense.md)  
 Explains how IntelliSense makes language references easy to access.  
  
 [Managed-Code Language Services with the MPF](../vs140/Implementing-a-Legacy-Language-Service1.md)  
 Provides information about how to use the managed package framework (MPF) to implement a full-featured language service in managed code.