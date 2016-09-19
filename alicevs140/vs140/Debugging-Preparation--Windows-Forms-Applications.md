---
title: "Debugging Preparation: Windows Forms Applications"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - VB
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7092ee7f-8378-4def-aef8-1695bd97cf14
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debugging Preparation: Windows Forms Applications
The Windows Forms project template creates a Windows Forms application. Debugging this type of application in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] is straightforward. For more information, see [Creating a Windows Application Project](assetId:///b2f93fed-c635-4705-8d0e-cf079a264efa).  
  
 When you create a Windows Forms project with the project template, [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] automatically creates required settings for the Debug and Release configurations. If necessary, you can change these settings. These settings can be changed in the **<project name\> Property Pages** dialog box (**My Project** in Visual Basic).  
  
 For more information, see [Managed Debugging: Recommended Property Settings](../Topic/Managed%20Debugging:%20Recommended%20Property%20Settings.md).  
  
 The following table displays one additional recommended property setting.  
  
### Configuration Properties in Debug tab  
  
|**Property Name**|**Setting**|  
|-----------------------|-----------------|  
|**Start Action**|-   Set to **Start project,** most of the time. Set to **Start external program** if you want to start another executable when you start debugging (usually for debugging DLLs).|  
  
 You can debug Windows Forms applications from inside [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], or by attaching to an already running application. For more information about attaching, see [Attach to Running Processes](../vs140/Attach-to-Running-Processes-with-the-Visual-Studio-Debugger.md).  
  
### To debug a C#, F#, or Visual Basic Windows Forms application  
  
1.  Open the project in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
2.  Create breakpoints as needed.  
  
     Because Windows Forms applications are event-driven, your breakpoints will go into event handler code, or into methods called by event handler code. Typical events in which to place breakpoints include:  
  
    1.  Events associated with a control, such as Click, Enter, etc.  
  
    2.  Events associated with application startup and shutdown, such as Load, Activated, etc.  
  
    3.  Focus and Validation Events.  
  
     For more information, see [Event Handling in Windows Forms](assetId:///6514e530-c6b8-489c-a8d2-eda7b7072701).  
  
3.  On the **Debug** menu, click **Start**.  
  
4.  Debug using the techniques discussed in [Debugger Basics](../vs140/Debugger-Basics.md).  
  
## See Also  
 [Debugging Managed Code](../Topic/Debugging%20Managed%20Code.md)   
 [Debugging Preparation: C#, F#, and Visual Basic Project Types](../vs140/Debugging-Preparation--C#--F#--and-Visual-Basic-Project-Types.md)   
 [How to: Set Debug and Release Configurations](../vs140/How-to--Set-Debug-and-Release-Configurations.md)   
 [Project Settings for C# and J# Debug Configurations](../vs140/Project-Settings-for--C#-Debug-Configurations.md)   
 [Project Settings for a Visual Basic Debug Configuration](../vs140/Project-Settings-for-a-Visual-Basic-Debug-Configuration.md)   
 [Attach to Running Processes](../vs140/Attach-to-Running-Processes-with-the-Visual-Studio-Debugger.md)   
 [Windows Forms](assetId:///627df1e9-b254-41af-bbac-9a4f02810c54)