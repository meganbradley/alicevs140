---
title: "Legacy Language Service Extensibility"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2700cd4d-5f68-43fc-b62f-dc80c3f3aa85
caps.latest.revision: 44
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Legacy Language Service Extensibility
A language service provides language-specific support for editing source code in the IDE.  
  
 Legacy language services are implemented as part of a VSPackage, but the newer way to implement language service features is to use MEF extensions. To find out more about the new way to implement a language service, see [Editor and Language Service Extensions](../vs140/Editor-and-Language-Service-Extensions.md).  
  
 This section discusses the structure and implementation of a legacy language service.  
  
## In This Section  
 [Migrating a Legacy Language Service](../vs140/Migrating-a-Legacy-Language-Service.md)  
 Explains how to update a language service from Visual Studio 2008 to the latest version.  
  
 [Language Services Essentials](../Topic/Legacy%20Language%20Service%20Essentials.md)  
 Provides important information about how to develop language services to integrate a programming language into Visual Studio.  
  
 [Developing a Legacy Language Service](../vs140/Developing-a-Legacy-Language-Service.md)  
 Provides links to topics that can help you create a language service.  
  
 [Providing A Syntax Coloring Service](../Topic/Syntax%20Coloring%20in%20a%20Legacy%20Language%20Service.md)  
 Provides information about supporting syntax highlighting in a language service.  
  
 [Managed-Code Language Services with the MPF](../vs140/Implementing-a-Legacy-Language-Service1.md)  
 Provides information about how to use the managed package framework (MPF) to implement a full-featured language service in managed code.  
  
 [Supporting Symbol-Browsing Tools](../Topic/Supporting%20Symbol-Browsing%20Tools.md)  
 Describes libraries and tools that enable you to browse tree views of symbols in the IDE.  
  
## Related Sections  
 [Visual Studio Editors](../vs140/Editor-and-Language-Service-Extensions.md)  
 Provides an overview of Visual Studio editors.  
  
 [Language Service Support for Debugging](../vs140/Language-Service-Support-for-Debugging.md)  
 Provides information about and a link to the Visual Studio Debugging SDK, which contains the information that is required to create and customize debugger components used to debug programs.