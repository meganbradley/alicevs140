---
title: "Extending Visual Studio Overview"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e9078d7-2763-4cc4-8e20-fac69d747f59
caps.latest.revision: 38
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extending Visual Studio Overview
The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE) provides the user interface (UI) for standard components, such as compilers, editors, and debuggers. Features like [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] and [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] that are included with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] are themselves extensions of the IDE. The [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] SDK provides tools, samples, wizards, designers, and documentation that helps you develop your own applications that extend the IDE and integrate seamlessly with it.  
  
## In This Section  
 [GettingStarted](../vs140/Starting-to-Develop-Visual-Studio-Extensions.md)  
 Provides an overview of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] SDK.  
  
 [User Experience Guidelines for Visual Studio](../vs140/Visual-Studio-User-Experience-Guidelines.md)  
 Provides guidelines for creating user interfaces for Visual Studio extensions.  
  
 [Managing Multiple Threads in Managed Code](../vs140/Managing-Multiple-Threads-in-Managed-Code.md)  
 Explains how to use background threads, and how to switch to the UI thread from a background thread.  
  
 [Visual Studio Integration Architecture](../vs140/VSSDK-Utilities.md)  
 Describes [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and its IDE, and introduces strategies and techniques for extending the IDE.  
  
 [VSIX Deployment](../vs140/Shipping-Visual-Studio-Extensions.md)  
 Describes how to use the VSIX format to package SDK projects. The VSIX format uses file-based deployment and does not support writing to the Global Assembly Cache (GAC) or to the system registry.  
  
 [Creating a Software Development Kit](../vs140/Creating-a-Software-Development-Kit.md)  
 Explains how to use a VSIX project to create your own SDK.  
  
 [Visual Studio Shell-Based Applications](../vs140/Shell--Isolated-or-Integrated-.md)  
 Explains how to create a custom tool that has its own integrated development environment (IDE). The Visual Studio SDK provides a project system, integration with editors and designers, source code control, and a familiar user interface that may reduce the learning curve for end users.  
  
 [User Interfaces](../vs140/Extending-Other-Parts-of-Visual-Studio.md)  
 Explains how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] services to create UI elements that match the rest of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Projects and Solutions](../vs140/Extending-Projects.md)  
 Describes how to use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] projects and solutions to organize code files and resource files, and how to implement source control.  
  
 [Reference Manager Extensibility](../Topic/Extending%20the%20Reference%20Manager.md)  
 Explains how to extend the Reference Manager.  
  
 [Visual Studio Editors](../vs140/Editor-and-Language-Service-Extensions.md)  
 Describes how to extend the Visual Studio editor and how to create custom editors.  
  
 [Language Services](../vs140/Legacy-Language-Service-Extensibility.md)  
 Describes how you can add support for a new programming language to [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Visual Studio Debugging Extensibility](../vs140/Visual-Studio-Debugger-Extensibility.md)  
 Describes how you can support debugging for a custom language.  
  
 [Data Designer Extensibility (DDEX) SDK](assetId:///29ee1968-f420-46aa-ba99-5fe710dc16bb)  
 Provides documentation, samples, and resources to help you implement a DDEX provider for exposing third-party data source objects in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Samples](../vs140/VSSDK-Samples.md)  
 Describes how to obtain Visual Studio Extensibility samples.  
  
 [VSPackage Walkthroughs](../vs140/Walkthroughs-for-Customizing-Visual-Studio-By-Using-VSPackages.md)  
 Describes how to create a basic VSPackage.  
  
## Related Sections  
 [Visual Studio SDK](../vs140/Visual-Studio-SDK.md)  
 Provides a gateway to documentation, samples, and code to help you develop products that integrate with the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] product family.  
  
 [Visual Studio](assetId:///06ddebea-2c83-4a45-bb48-6264c797ed93)  
 Discusses how to develop applications by using [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. Includes sections about how to extend the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] IDE by using add-ins.