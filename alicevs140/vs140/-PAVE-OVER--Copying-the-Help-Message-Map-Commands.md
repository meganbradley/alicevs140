---
title: "&lt;PAVE OVER&gt; Copying the Help Message Map Commands"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 52360000-a3bc-4fd5-a77d-ffb703c66148
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Copying the Help Message Map Commands
The MFC Application Wizard places help-specific code into the message map in the frame window class implementation file, MainFrm.cpp.  
  
### To copy help-related code to your project  
  
1.  Open the HasHelp project MainFrm.cpp file and your project's version of MainFrm.cpp.  
  
2.  Scroll to the Help-related code, delineated by the `//global help commands` comment, in the message map section of the HasHelp MainFrm.cpp file.  
  
3.  Copy this code, shown below, from the HasHelp MainFrm.cpp file, and paste into the same position in the message map in your MainFrm.cpp.  
  
    ```  
    // Global help commands  
    ON_COMMAND(ID_HELP_FINDER, CMDIFrameWnd::OnHelpFinder)  
    ON_COMMAND(ID_HELP, CMDIFrameWnd::OnHelp)  
    ON_COMMAND(ID_CONTEXT_HELP, CMDIFrameWnd::OnContextHelp)  
    ON_COMMAND(ID_DEFAULT_HELP, CMDIFrameWnd::OnHelpFinder)  
    ```  
  
     You have already seen how **ID_HELP_FINDER** and **ID_CONTEXT_HELP** are called. When the user presses F1, the framework calls `ID_HELP` and directly handles this command so long as the application contains help support.  
  
4.  Close the HasHelp project's MainFrm.cpp file, and save the changes to your project's MainFrm.cpp.  
  
## See Also  
 [Adding HTML Help Context-Sensitive Help to an Existing MFC Application](../vs140/-PAVE-OVER--Adding-HTML-Help-Context-Sensitive-Help-to-an-Existing-MFC-Application.md)