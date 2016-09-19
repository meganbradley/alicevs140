---
title: "Start  the Remote Debugging Monitor"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 55b60ce7-834b-4e83-a10e-fe4248260a4c
caps.latest.revision: 55
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Start  the Remote Debugging Monitor
The Remote Debugging Monitor (msvsmon.exe) is a small application that [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] connects to for remote debugging. During remote debugging, [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] runs on one computer (the debugger host) and the Remote Debugging Monitor runs on a remote computer together with the applications that you are debugging.  
  
 Before you can start remote debugging, you must set up remote debugging. For more information, see [How to: Set Up Remote Debugging](../vs140/Set-Up-the-Remote-Tools-on-the-Device.md).  
  
> [!NOTE]
>  The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition. To change your settings, choose **Import and Export Settings** on the **Tools** menu. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
 **Permissions**  
  
 The Visual Studio user must have permission to connect to the remote debugger. By default, administrators on the remote machine can connect to the remote debugger. To grant permissions to other users, see[Configuring the remote debugger](../vs140/Set-Up-the-Remote-Tools-on-the-Device.md#BKMK_Configuring_the_remote_debugger).  
  
 For information about permissions for remote debugging across domains or between workgroup computers, see [Remote Debugging Across Domains](../vs140/Remote-Debugging-Across-Domains.md).  
  
### To start the remote debugging monitor  
  
1.  On the remote computer, find **Visual Studio 2013 Remote Debugger** on the **Start** menu.  
  
     -or-  
  
     Run msvsmon.exe at the Windows Command Prompt.  
  
     The **Remote Debugging Monitor** runs as a Windows application. The user interface shows that the **Remote Debugging Monitor** is running and makes remote debugging easy to set up.  
  
## Running the Remote Debugging Service (ASP.NET and Other Server Environments)  
 For debugging in [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] and other server environments, you can run the Remote Debugging Monitor as a Windows service (the Remote Debugger Service.)  
  
#### To configure the remote debugging monitor as a service  
  
1.  Find **Visual Studio Remote Debugger Configuration Wizard** on the **Start** menu.  
  
2.  Follow the steps in the wizard to set up remote debugging as a service.  
  
## See Also  
 [Debugging in Visual Studio](../vs140/Debugging-in-Visual-Studio.md)   
 [Remote Debugging](../vs140/Remote-Debugging.md)   
 [How to: Set Up Remote Debugging](../vs140/Set-Up-the-Remote-Tools-on-the-Device.md)   
 [Remote Debugging Across Domains](../vs140/Remote-Debugging-Across-Domains.md)   
 [Remote Debugging Errors and Troubleshooting](../vs140/Remote-Debugging-Errors-and-Troubleshooting.md)   
 [Just-In-Time Debugging](../Topic/Just-In-Time%20Debugging%20in%20Visual%20Studio.md)