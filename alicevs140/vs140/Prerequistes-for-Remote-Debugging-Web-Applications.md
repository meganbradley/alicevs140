---
title: "Prerequistes for Remote Debugging Web Applications"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1cd777b5-6d20-4ca6-a0df-51653b118469
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Prerequistes for Remote Debugging Web Applications
With the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugger, you can debug a Web application transparently on the local computer or a remote server. This means that the debugger functions the same way and allows you to use the same features on either computer. For remote debugging to work correctly, however, there are some prerequisites.  
  
-   [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] remote debugging components must be installed on the server you want to debug. For more information, see [Setting Up Remote Debugging](../vs140/Set-Up-the-Remote-Tools-on-the-Device.md).  
  
-   By default, the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process runs as an ASPNET user process. As a result, you must have Administrator privileges on the computer where [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] runs to debug it. The name of the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process varies by debug scenario and version of IIS. For more information, see [How to: Find the Name of the ASP.NET Process](../vs140/How-to--Find-the-Name-of-the-ASP.NET-Process.md).  
  
## See Also  
 [Debugging ASP.NET and AJAX Applications](../vs140/Debugging-ASP.NET-and-AJAX-Applications.md)   
 [ASP.NET Debugging: System Requirements](../vs140/ASP.NET-Debugging--System-Requirements.md)