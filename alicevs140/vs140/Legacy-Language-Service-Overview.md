---
title: "Legacy Language Service Overview"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bb44e27b-d228-463c-b2cf-cd5c24c7c1b5
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Legacy Language Service Overview
A language service provides editor support that lets you implement certain [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] features. The Managed Package Framework (MPF) language service classes provide full support for frequently-used features and partial support for other features.  
  
## Fully Supported Features in the MPF  
 The MPF language service classes support the following features:  
  
-   Syntax highlighting  
  
-   Outlining  
  
-   Commenting blocks of code  
  
-   Brace matching  
  
-   Code snippets  
  
-   Custom document properties  
  
-   IntelliSense parameter information  
  
-   IntelliSense Quick Info  
  
-   IntelliSense member completion  
  
-   IntelliSense word completion  
  
## Partially Supported Features in the MPF  
 The MPF provides only partial support for the following features. This means that you must implement the methods that are called by the MPF.  
  
-   Reformatting code. You supply the code that implements the reformatting.  
  
-   Validating breakpoints by identifying valid code spans. You supply the code that identifies the code spans.  
  
-   Supporting the debugger **Autos** window for displaying variables. You supply the code that determines what to show in the window.  
  
-   Supporting the **Navigation bar** for quick navigation between types and members. You implement and return a helper class that populates the lists in the **Navigation bar** combo boxes.  
  
## Implementation  
 You must complete several steps to implement the language service itself and the language service features that you want to support for your language. These steps are discussed in the following topics:  
  
-   [Implementing a Language Service (Managed Package Framework)](../Topic/Implementing%20a%20Legacy%20Language%20Service2.md)  
  
-   [Registering a Language Service (Managed Package Framework)](../vs140/Registering-a-Legacy-Language-Service1.md)  
  
-   [Syntax Highlighting (Managed Package Framework)](../Topic/Syntax%20Colorizing%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Brace Matching (Managed Package Framework)](../Topic/Brace%20Matching%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Outlining (Managed Package Framework)](../Topic/Outlining%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Commenting Blocks of Code (Managed Package Framework)](../vs140/Commenting-Code-in-a-Legacy-Language-Service.md)  
  
-   [Reformatting Code (Managed Package Framework)](../Topic/Reformatting%20Code%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Custom Document Properties (Managed Package Framework)](../Topic/Custom%20Document%20Properties%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Supporting Code Snippets (Managed Package Framework)](../vs140/Support-for-Code-Snippets-in-a-Legacy-Language-Service.md)  
  
-   [Supporting the Navigation Bar (Managed Package Framework)](../vs140/Support-for-the-Navigation-Bar-in-a-Legacy-Language-Service.md)  
  
-   [Supporting IntelliSense Complete Word (Managed Package Framework)](../Topic/Word%20Completion%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Supporting IntelliSense Member Completion (Managed Package Framework)](../Topic/Member%20Completion%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Supporting IntelliSense Parameter Info (Managed Package Framework)](../Topic/Parameter%20Info%20in%20a%20Legacy%20Language%20Service2.md)  
  
-   [Supporting IntelliSense Quick Info (Managed Package Framework)](../Topic/Quick%20Info%20in%20a%20Legacy%20Language%20Service.md)  
  
-   [Supporting the Autos Window (Managed Package Framework)](../vs140/Support-for-the-Autos-Window-in-a-Legacy-Language-Service.md)  
  
-   [Validating Breakpoints (Managed Package Framework)](../Topic/Validating%20Breakpoints%20in%20a%20Legacy%20Language%20Service.md)  
  
## See Also  
 [Language Service in the Managed Package Framework](../vs140/Implementing-a-Legacy-Language-Service1.md)   
 [Language Services](../vs140/Legacy-Language-Service-Extensibility.md)