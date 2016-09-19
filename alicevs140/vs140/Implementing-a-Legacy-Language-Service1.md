---
title: "Implementing a Legacy Language Service1"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
H1: Implementing a Legacy Language Service
ms.assetid: df638f24-166d-4b80-be82-c9c39ca7a556
caps.latest.revision: 20
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Implementing a Legacy Language Service1
You can use classes in the managed package framework (MPF) to implement a legacy language service that supports a wide variety of features, such as syntax highlighting, brace matching, and IntelliSense completion.  
  
 Legacy language services are implemented as part of a VSPackage, but the newer way to implement language service features is to use MEF extensions. To find out more about the new way to implement a language service, see [Editor and Language Service Extensions](../vs140/Editor-and-Language-Service-Extensions.md).  
  
> [!NOTE]
>  We recommend that you begin to use the new editor API as soon as possible. This will improve the performance of your language service and let you take advantage of new editor features.  
  
## In This Section  
 [Language Service Overview (Managed Package Framework)](../vs140/Legacy-Language-Service-Overview.md)  
 An overview of the language service features that are supported in MPF.  
  
 [Implementing a Language Service (Managed Package Framework)](../Topic/Implementing%20a%20Legacy%20Language%20Service2.md)  
 Describes what is required to implement a language service by using MPF.  
  
 [Registering a Language Service (Managed Package Framework)](../vs140/Registering-a-Legacy-Language-Service1.md)  
 Describes the steps that are required to register an MPF-based language service with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [The Language Service Parsers (Managed Package Framework)](../Topic/Legacy%20Language%20Service%20Parser%20and%20Scanner.md)  
 Describes the two parsers that are required to implement all the features of a language service by using the MPF.  
  
 [Walkthrough: Creating a Language Service (Managed Package Framework)](../Topic/Walkthrough:%20Creating%20a%20Legacy%20Language%20Service.md)  
 Provides the basic steps that are required to implement an MPF language service in a VSPackage.  
  
 [How to: Get a List of Installed Code Snippets](../Topic/Walkthrough:%20Getting%20a%20List%20of%20Installed%20Code%20Snippets%20\(Legacy%20Implementation\).md)  
 Demonstrates the techniques of retrieving a list of installed code snippets.  
  
 [Language Service Features (Managed Package Framework)](../vs140/Legacy-Language-Service-Features1.md)  
 Provides links to topics that detail what must be done to implement all the features of a language service by using MPF.