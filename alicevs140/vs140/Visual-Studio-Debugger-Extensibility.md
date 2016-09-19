---
title: "Visual Studio Debugger Extensibility"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c088b6a2-c3ad-446b-830d-9c6f41b2934b
caps.latest.revision: 34
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Visual Studio Debugger Extensibility
Visual Studio includes a fully interactive source code debugger, providing a powerful and easy-to-use tool for tracking down bugs in your program. The debugger has complete support Visual Basic, C#, C/C++, and JavaScript. However, with the [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)], that is available from the [Microsoft Download Center](http://go.microsoft.com/fwlink/?LinkId=214453),, other programming languages can be supported in the debugger with the same rich features.  
  
 The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugger is the common front end (that is, the user interface) to the debugging components that are, in turn, specific to the language being debugged. For new languages, all that is necessary for support by the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugger is to create the necessary back-end components, such as a debug engine (DE). That is where the [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)] comes in.  
  
 The [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)] includes a complete reference to all [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] elements required to create a new DE. In addition, there are samples and tutorials that will help get you started.  
  
 For an end-to-end sample of a language project system with debugging support, see the [IronPython sample](assetId:///4c41695c-12c1-4670-b43b-d8d84c9e4089).  
  
 The following sections describe how to extend the debugger by using the [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)].  
  
## In This Section  
 [Getting Started](../vs140/Getting-Started-with-Debugger-Extensibility.md)  
 Describes what [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Debugging offers and how to install the SDK.  
  
 [Creating a Custom Debug Engine](../vs140/Creating-a-Custom-Debug-Engine.md)  
 Documents the custom DE process, from preparing your program for a DE to detaching the DE.  
  
 [Writing a CLR Expression Evaluator](../vs140/Writing-a-Common-Language-Runtime-Expression-Evaluator.md)  
 Explains whether you must write an expression evaluator.  
  
 [Choosing a Debug Engine Implementation Strategy](../vs140/Choosing-a-Debug-Engine-Implementation-Strategy.md)  
 Discusses how to implement your DE.  
  
 [Reference](../vs140/Reference--Visual-Studio-Debugging-APIs-.md)  
 Documents the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Debugging API.  
  
 [Samples](../vs140/Visual-Studio-Debugging-Samples.md)  
 Contains links to a common language runtime expression evaluator sample and a debug engine sample.