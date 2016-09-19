---
title: "Getting Started with Debugger Extensibility"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6ce6f43-1409-4bf7-93cd-f3464ca23504
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Getting Started with Debugger Extensibility
The [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)] provides the information that you must have to create and customize debugger components used to debug programs from within the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] environment.  
  
 [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugging has added improvements derived from the extensive usability testing performed on previous [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debuggers. You can use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugging to step through a multi-language application, or you can implement on-the-fly editing of variables while debugging applications and multi-language solutions.  
  
 [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugging is executed out-of-process with the program being debugged and is therefore less intrusive in the process space of the application. Consequently, it is easier to write components that interact with the debugger without affecting your debugging program.  
  
 To best use the [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)], you should be familiar with the following:  
  
-   The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE)  
  
-   The C++ programming language  
  
-   ATL COM  
  
## In This Section  
 [Roadmap for Extending the Debugger](../vs140/Roadmap-for-Extending-the-Debugger.md)  
 Outlines the process of implementing debugging in your product, depending on your compiler and its output.  
  
 [Debugger Components](../vs140/Debugger-Components.md)  
 Provides an overview of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugging components, which include the debug engine (DE), expression evaluator (EE), and symbol handler (SH).  
  
 [Debugger Concepts](../vs140/Debugger-Concepts.md)  
 Describes the main debugging architectural concepts.  
  
 [Debugger Contexts](../vs140/Debugger-Contexts.md)  
 Explains how the debug engine (DE) operates simultaneously within code, documentation, and expression evaluation contexts. Describes, for each of the three contexts, the location, position or evaluation relevant to it.  
  
 [Debugging Tasks](../vs140/Debugging-Tasks.md)  
 Contains links to various debugging tasks, such as launching a program and evaluating expressions.