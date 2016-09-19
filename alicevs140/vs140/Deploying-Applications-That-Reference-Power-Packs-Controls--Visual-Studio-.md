---
title: "Deploying Applications That Reference Power Packs Controls (Visual Studio)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f2230f53-a745-4731-89e6-033943faa209
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Deploying Applications That Reference Power Packs Controls (Visual Studio)
If you want to deploy an application that references the Power Packs controls (<xref:Microsoft.VisualBasic.PowerPacks.LineShape?qualifyHint=False>, <xref:Microsoft.VisualBasic.PowerPacks.OvalShape?qualifyHint=False>, <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape?qualifyHint=False>, or <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>), the controls must be installed on the destination computer.  
  
## Installing the Power Packs Controls as a Prerequisite  
 To successfully deploy an application, you must also deploy all components that are referenced by the application. The process of installing prerequisite components is known as *bootstrapping*.  
  
 When [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] is installed on your development computer, a Power Packs bootstrapper package is added to the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] bootstrapper directory. This package is then available when you follow the procedures for adding prerequisites for either [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] or Windows Installer deployment.  
  
 By default, bootstrapped components are deployed from the same location as the installation package. Alternatively, you can choose to deploy the components from a URL or file share location from which users can download them as necessary.  
  
> [!NOTE]
>  To install bootstrapped components, the user might need administrative or similar user permissions on the computer. For [!INCLUDE[ndptecclick](../vs140/includes/ndptecclick_md.md)] applications, this means that the user will need administrative permissions to install the application, regardless of the security level specified by the application. After the application is installed, the user can run the application without administrative permissions.  
  
 During installation, users will be prompted to install the Power Packs controls if they are not present on the destination computer.  
  
 As an alternative to bootstrapping, you can pre-deploy the Power Packs controls by using an electronic software distribution system such as Microsoft Systems Management Server.  
  
## See Also  
 [How to: Install Prerequisites in Windows Installer Deployment](assetId:///653fc868-2486-429c-b75e-2f9d0c7f6619)   
 [How to: Install Prerequisites with a ClickOnce Application](../vs140/How-to--Install-Prerequisites-with-a-ClickOnce-Application.md)   
 [Not in Build: Choosing a Deployment Strategy](assetId:///ecd632d8-063c-4028-b785-81bba045107b)   
 [Visual Basic Power Packs Controls](../Topic/Visual%20Basic%20Power%20Packs%20Controls.md)