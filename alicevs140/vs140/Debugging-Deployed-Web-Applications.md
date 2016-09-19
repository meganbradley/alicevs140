---
title: "Debugging Deployed Web Applications"
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
ms.assetid: b938a91b-be96-416f-83bc-4177e7f3929a
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debugging Deployed Web Applications
If you need to debug a Web application that is running on a production server, this should be done with caution. If you attach to the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process for debugging and hit a breakpoint, for example, all managed code in the worker process halts. Halting all managed code in the worker process can cause a work stoppage for all users on the server. Before you debug on a production server, consider the potential impact on production work.  
  
 To use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] to debug a deployed application, you must attach to the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process and make sure that the debugger has access to symbols for the application. You must also locate and open the source files for the application. For more information, see [Managing Symbols and Source Code](../vs140/Specify-Symbol--.pdb--and-Source-Files-in-the-Visual-Studio-Debugger.md), [How to: Find the Name of the ASP.NET Process](../vs140/How-to--Find-the-Name-of-the-ASP.NET-Process.md), and [ASP.NET Debugging: System Requirements](../vs140/ASP.NET-Debugging--System-Requirements.md).  
  
> [!NOTE]
>  Many [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] Web applications reference DLLs that contain business logic or other useful code. Such a reference automatically copies the DLL from your local computer to the \bin folder of the Web application's virtual directory. When you are debugging, remember that your Web application is referencing that copy of the DLL and not the copy on your local computer.  
  
 The process for attaching to the [!INCLUDE[vstecasp](../vs140/includes/vstecasp_md.md)] worker process is the same as attaching to any other remote process. When you are attached, if you do not have the correct project open, a dialog box appears when the application breaks. This dialog box asks for the location of the source files for the application. The file name that you specify in the dialog box must match the file name specified in the debug symbols on the Web server. For more information, see [Attaching to Running Processes](../vs140/Attach-to-Running-Processes-with-the-Visual-Studio-Debugger.md).  
  
## See Also  
 [Debugging ASP.NET and AJAX Applications](../vs140/Debugging-ASP.NET-and-AJAX-Applications.md)   
 [Debugging Web Applications and Script](../vs140/Debugging-Web-Applications-and-Script.md)   
 [How to: Enable Debugging for ASP.NET Applications](../vs140/How-to--Enable-Debugging-for-ASP.NET-Applications.md)   
 [How to: Find the Name of the ASP.NET Process](../vs140/How-to--Find-the-Name-of-the-ASP.NET-Process.md)   
 [Managing Symbols and Source Code](../vs140/Specify-Symbol--.pdb--and-Source-Files-in-the-Visual-Studio-Debugger.md)