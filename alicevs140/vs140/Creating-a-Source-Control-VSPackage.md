---
title: "Creating a Source Control VSPackage"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cca0a9ed-48ff-409f-8036-ed8db0f7533e
caps.latest.revision: 25
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Creating a Source Control VSPackage
This documentation includes links to the architecture overview of a source-control package integrated with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], the API that is defined by the interfaces to be implemented and the services to be consumed, and a sample that illustrates a simple source control package implementation.  
  
 With a source control VSPackage, you can create a deep integration path for source control to integrate with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. It enables the package to bypass the default source control UI hosted by [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], respond to source control requests from the project system, and interact with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] components such as **Solution Explorer**. The [!INCLUDE[vsipsdk](../vs140/includes/vsipsdk_md.md)] empowers [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] partners with a mechanism to create a VSPackage that can integrate with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] using a service model.  
  
## In This Section  
 [Getting Started](../vs140/Getting-Started-with-Source-Control-VSPackages.md)  
 Discusses the source control package, which is a more advanced alternative to the source control plug-in for implementing source control features in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Source Control Package Architecture Overview](../vs140/Source-Control-VSPackage-Architecture.md)  
 Presents a diagram and explains the components of a source control package.  
  
 [Source Control Package Features](../vs140/Source-Control-VSPackage-Features.md)  
 Describes the various features of a source control package.  
  
 [Design Elements](../vs140/Source-Control-VSPackage-Design-Elements.md)  
 Describes the structure of the VSPackage that a source control package must implement for deep integration.  
  
## Related Sections  
 [Creating a Source Control Plug-in](../vs140/Creating-a-Source-Control-Plug-in.md)  
 Discusses how to create a source control plug-in that supplies source control functionality in the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] source control user interface (UI).  
  
 [Source Control (Visual Studio SDK)](../vs140/Source-Control.md)  
 Discusses the options for implementing source control as an integrated feature of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].