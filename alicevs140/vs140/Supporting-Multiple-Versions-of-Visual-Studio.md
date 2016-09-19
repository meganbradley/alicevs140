---
title: "Supporting Multiple Versions of Visual Studio"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0047aa90-1ed4-40d3-8772-622b2719a4b1
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Supporting Multiple Versions of Visual Studio
The term *side-by-side* means that you can install and maintain multiple versions of a product on the same computer. For VSPackages, that means a user can have several Visual Studio versions installed on the same computer. However, you cannot have side-by-side versions of your VSPackages loaded into a single version of Visual Studio.  
  
 Before you make your VSPackage able to be loaded into side-by-side versions of Visual Studio, consider the following:  
  
-   You must determine which side-by-side implementation strategy you want to follow.  
  
     For more information, see [Choosing Between Shared and Versioned VSPackages](../vs140/Choosing-Between-Shared-and-Versioned-VSPackages.md).  
  
-   Your solution and project file formats must fit your implementation strategy.  
  
     For more information, see [How to: Upgrade a Project System](../Topic/Upgrading%20Custom%20Projects.md) and [Registering File Name Extensions for Side-By-Side Deployments](../vs140/Registering-File-Name-Extensions-for-Side-By-Side-Deployments.md).  
  
-   Your installer must handle your implementation strategy so that versioned components, and also components shared across all versions, are correctly installed and registered.  
  
     For more information, see [Installing VSPackages With Windows Installer](../vs140/Installing-VSPackages-With-Windows-Installer.md) and also [Component Management](../vs140/Component-Management.md).  
  
    > [!NOTE]
    >  Installing a version of Visual Studio also installs a corresponding version of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]. For example, installing Visual Studio 2010 and Visual Studio 2012 on the same computer also installs versions 4.0 and 4.5 of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)], respectively.  
  
## In This Section  
 [Choosing Between Shared and Versioned VSPackages](../vs140/Choosing-Between-Shared-and-Versioned-VSPackages.md)  
 Explains how to resolve side-by-side issues in your VSPackage.  
  
 [Registering File Extensions for Side-By-Side Deployments](../vs140/Registering-File-Name-Extensions-for-Side-By-Side-Deployments.md)  
 Describes how your VSPackage can register file associations in a side-by-side scenario.  
  
## Related Sections  
 [Installing VSPackages](../vs140/Installing-VSPackages.md)  
 Discusses how to build and install VSPackages and how to support users who are running multiple versions of Visual Studio at the same time.