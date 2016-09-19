---
title: "Installing VSPackages With Windows Installer"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 41d2c72c-0a97-4fcd-b3aa-33a8d3aa962a
caps.latest.revision: 32
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Installing VSPackages With Windows Installer
Integrating your VSPackage into [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] requires more than just copying files to a user's computer. Your VSPackage's installer must install the VSPackage and its dependent files, and register and integrate them into [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. Your VSPackage can take advantage of integration features such as displaying an icon on the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] splash screen and About dialog box.  
  
 Microsoft Windows Installer files are the recommended way to distribute your VSPackages. Easy-to-use Windows Installer packages can run on any Windows operating system supported by [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. For more information, see [Windows Installer](assetId:///121be21b-b916-43e2-8f10-8b080516d2a0).  
  
## In This Section  
 [Windows Installer Basics](../vs140/Windows-Installer-Basics.md)  
 Provides an overview of the Windows Installer.  
  
 [VSPackage Setup Scenarios](../vs140/VSPackage-Setup-Scenarios.md)  
 Discusses different ways you can support side-by-side installations of both your VSPackages and [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Authoring a Windows Installer Package](../vs140/Authoring-a-Windows-Installer-Package.md)  
 Provides an overview of the typical steps installers follow to correctly install and integrate VSPackages into [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Detecting System Requirements](../vs140/Detecting-System-Requirements.md)  
 Describes how an installer can detect [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and its components and cancel setup if VSPackage requirements are not met.  
  
 [Component Management](../vs140/Component-Management.md)  
 Discusses how to develop an installer that will maintain the integrity of previous product versions.  
  
 [Choosing a VSPackage Installation Directory](../vs140/Choosing-the-Installation-Directory-for-a-VSPackage.md)  
 Summarizes the options for locating VSPackages.  
  
 [VSPackage Registration](../vs140/VSPackage-Registration.md)  
 Discusses how VSPackages are registered at installation time and why self-registration is a bad idea.  
  
 [Deploying Managed-Code Project Types](../vs140/Deploying-Project-Types.md)  
 Discusses how to use the new project-type aggregator for managed-code project types.  
  
 [How to: Generate Registry Information for an Installer (C#)](../vs140/How-to--Generate-Registry-Information-for-an-Installer.md)  
 Explains how to use RegPkg.exe to generate a registration manifest for a managed VSPackage.  
  
 [Post-install Commands](../vs140/Commands-That-Must-Be-Run-After-Installation.md)  
 Explains how to run post-installation commands to integrate VSPackages into [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [Uninstalling Your VSPackage](../vs140/Uninstalling-a-VSPackage-With-Windows-Installer.md)  
 Describes the steps your installer must perform when users uninstall your VSPackage.  
  
## Related Sections  
 [Installing VSPackages](../vs140/Installing-VSPackages.md)  
 Discusses how to build and install VSPackages and how to support users who are running multiple versions of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] at the same time.