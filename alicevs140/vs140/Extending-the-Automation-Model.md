---
title: "Extending the Automation Model"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f09e1365-6291-41a7-b52b-9398270d9da2
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Extending the Automation Model
This section discusses how the automation model and the VSPackage model represent a two-prong approach to extensibility in the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] environment. Extensibility is the capacity to enhance and extend the functionality of the IDE. Automation, on the one hand, refers to user-created code and tools that automate tasks in the existing environment and programmatically drive the IDE. VSPackages, on the other hand, let you add new functionality to the environment.  
  
 It is possible to combine automation and VSPackages in an extensibility application. For an example, see [Walkthrough: Extending Managed VSPackages with Automation](../Topic/Walkthrough:%20Extending%20Managed%20VSPackages%20By%20Using%20Automation.md).  
  
 For an end-to-end sample of a language project system that supports the automation model, see the [IronPython sample](../vs140/VSSDK-Samples.md).  
  
## In This Section  
 [Automation Model](../Topic/Automation%20Model.md)  
 Provides an overview of the automation model and discusses how the automation model lets you customize, adjust, and automate the environment.  
  
 [Contributing to the Automation Model](../vs140/Contributing-to-the-Automation-Model.md)  
 Provides a more detailed view of the automation model and discusses the ways to provide automation for your VSPackage. This section also provides code examples that show how an automation consumer obtains the initial project automation objects.  
  
## Related Sections  
 [Visual Studio SDK and Automation](../vs140/Visual-Studio-SDK-and-Automation.md)  
 Discusses using automation, VSPackages, or a combination to create [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] extensibility applications.