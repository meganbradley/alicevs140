---
title: "Developing a Legacy Language Service"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6151ba88-c1c3-41de-a1cc-668f494d48d1
caps.latest.revision: 30
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Developing a Legacy Language Service
This section links to topics that help you create a legacy language service.  
  
 Legacy language services are implemented as part of a VSPackage, but the newer way to implement language service features is to use MEF extensions. To find out more about the new way to implement a language service, see [Editor and Language Service Extensions](../vs140/Editor-and-Language-Service-Extensions.md).  
  
> [!NOTE]
>  We recommend that you begin to use the new editor API as soon as possible. This will improve the performance of your language service and let you take advantage of new editor features.  
  
## In This Section  
 [Model of a Legacy Language Service](../vs140/Model-of-a-Legacy-Language-Service.md)  
 Provides a model of a minimal language service for the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] core editor. You can use this model as a guide for creating your own language service.  
  
 [Legacy Language Service Interfaces](../Topic/Legacy%20Language%20Service%20Interfaces.md)  
 Discusses the objects required to implement a language service and provides a listing of additional objects that you can use to provide syntax highlighting, method data, and other features.  
  
 [Intercepting Legacy Language Service Commands](../Topic/Intercepting%20Legacy%20Language%20Service%20Commands.md)  
 Describes how to insert a command filter into your language service to intercept commands that the text view would otherwise handle.  
  
 [Registering a Language Service](../Topic/Registering%20a%20Legacy%20Language%20Service2.md)  
 Provides information about how to register your language service by using [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Language Service Support for Debugging](../vs140/Language-Service-Support-for-Debugging.md)  
 Describes how a language service can provide features to support a debugger.  
  
 [Checklist: Creating a Language Service](../Topic/Checklist:%20Creating%20a%20Legacy%20Language%20Service.md)  
 Provides step-by-step instructions for creating and integrating a language service for the core editor.  
  
## Related Sections  
 [Syntax Coloring in a Legacy Language Service](../Topic/Syntax%20Coloring%20in%20a%20Legacy%20Language%20Service.md)  
 Discusses how to implement syntax highlighting in your language service.  
  
 [Statement Completion in a Legacy Language Service](../vs140/Statement-Completion-in-a-Legacy-Language-Service.md)  
 Discusses statement completion, the process by which a language service helps users finish a language keyword or element that they have started typing.  
  
 [Parameter Info in a Legacy Language Service](../Topic/Parameter%20Info%20in%20a%20Legacy%20Language%20Service1.md)  
 Describes how to provide method tips for overloaded functions and methods.  
  
 [How to: Provide Hidden Text Support](../vs140/How-to--Provide-Hidden-Text-Support-in-a-Legacy-Language-Service.md)  
 Explains the purpose of a hidden text region and provides instructions about how to implement a hidden text region.  
  
 [How to: Provide Expanded Outlining Support](../Topic/How%20to:%20Provide%20Expanded%20Outlining%20Support%20in%20a%20Legacy%20Language%20Service.md)  
 Explains the two options that extend outlining support for your language beyond supporting the *Collapse to Definitions* command.