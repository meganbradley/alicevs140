---
title: "ASP.NET Debugging: System Requirements"
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
ms.assetid: 7810b9b2-debf-4271-8fc7-1df031123255
caps.latest.revision: 40
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ASP.NET Debugging: System Requirements
This topic describes the software and security requirements for [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] debugging scenarios:  
  
-   Local debugging, in which [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] and the Web application run on the same computer. There are two versions of this scenario:  
  
    -   The [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] code resides on the file system.  
  
    -   The [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] code resides in an IIS Web site.  
  
-   Remote debugging, in which [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] runs on a client computer and debugs a Web application that is running on a remote server computer.  
  
## Security Requirements  
 For remote debugging, local and remote computers must be on a domain setup or a workgroup setup.  
  
 To debug the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process you must have permission to debug that process. By default, [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] applications run as the **ASPNET** user. If the worker process is running as **ASPNET**, or as **NETWORK SERVICE**, you must have Administrator privileges to debug it.  
  
 The name of the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process varies by debugging scenario and by version of IIS. For more information, see [How to: Find the Name of the ASP.NET Process](../vs140/How-to--Find-the-Name-of-the-ASP.NET-Process.md).  
  
 You can change the user account that the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process runs under by editing the machine.config file on the server that is running IIS. The best way to do this is to use the **Internet Information Services (IIS) Manager**. For more information, see [How to: Run aspnet_wp.exe Under a User Account](../vs140/How-to--Run-the-Worker-Process-Under-a-User-Account.md).  
  
 If you change the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process to run under your own user account, you do not have to be an Administrator on the server that is running IIS.  
  
> [!CAUTION]
>  Before you change the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process to run under a different account, consider the possible consequences if the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process should be hacked while running under that account. The ASPNET and NETWORK SERVICE user accounts run with minimal permissions, reducing the possible damage if the process is hacked. If you must change the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process to run under an account that has greater permissions, the potential damage is greater.  
  
## See Also  
 [Debugging ASP.NET and AJAX Applications](../vs140/Debugging-ASP.NET-and-AJAX-Applications.md)   
 [How to: Run aspnet_wp.exe Under a User Account](../vs140/How-to--Run-the-Worker-Process-Under-a-User-Account.md)