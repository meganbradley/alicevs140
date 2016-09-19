---
title: "Just-In-Time, Debugging, Options Dialog Box"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
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
ms.assetid: 7f11b2e3-3fb5-449d-b07c-6ecf1d6a487d
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Just-In-Time, Debugging, Options Dialog Box
To access the **Just-In-Time** page, go to the **Tools** menu and click **Options**. In the **Options** dialog box, expand the **Debugging** node and select **Just-In-Time**. This page allows you to enable Just-In-Time debugging for managed code, native code, and script. For more information, see [Just-In-Time Debugging](../Topic/Just-In-Time%20Debugging%20in%20Visual%20Studio.md).  
  
 You can enable Just-In-Time debugging for these program types:  
  
-   Managed  
  
-   Native  
  
-   Script  
  
 Just-In-Time debugging is a technique for debugging a program that is started outside [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]. You can run a program created in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] outside of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] environment. If you have enabled Just-in-time debugging, a crash will display a dialog box that asks if you want to debug.  
  
## Associated Warnings  
 When you visit this page of the **Options** dialog box, you might see a warning message like this:  
  
 **Another debugger has registered itself as the Just-In-Time debugger. To repair, enable Just-In-Time debugging or run Visual Studio repair.**  
  
 This message occurs if you have another debugger, possibly an older version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] debugger, set as the Just-In-Time debugger.  
  
 Another message that you might see is as follows:  
  
 **Just-In-Time debugging registration errors detected. To repair, enable Just-In-Time debugging or run Visual Studio repair.**  
  
 If you see either of these warnings, Just-In-Time debugging with [!INCLUDE[vs_dev11_long](../vs140/includes/vs_dev11_long_md.md)] requires Administrator privileges until you have fixed the problem. If you try to enable just-as a non-administrator under these conditions, you will see the following error message:  
  
 **Access is denied. Have an administrator enable Just-In-Time debugging, or repair your installation of Visual Studio.**  
  
## See Also  
 [Debugging, Options Dialog Box](../vs140/Debugging--Options-Dialog-Box.md)   
 [How to: Specify Debugger Settings](../vs140/How-to--Specify-Debugger-Settings.md)