---
title: "&lt;PAVE OVER&gt; Copying the Help Accelerator Resources"
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
ms.assetid: 6b4e30f6-0db2-439f-b80e-a8c04b4265e8
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Copying the Help Accelerator Resources
Next, copy the accelerator resources for the menu items.  
  
### To copy the accelerator keys for Help resources  
  
1.  Open the Accelerator table resource, **IDR_MAINFRAME**, from both your project and HasHelp, resizing the accelerator editor windows, as described in [Copying the Help Menu Resources](../vs140/-PAVE-OVER--Copying-the-Help-Menu-Resources.md), so they do not overlap.  
  
2.  Select the `ID_HELP` command from the HasHelp Accelerator table.  
  
3.  Hold down the CTRL key while you drag this entry to your project's accelerator editor window.  
  
     It doesn't matter where in the window you drop the entry. This copies the accelerator keys (F1 and SHIFT+F1) for the Help menu item to your project.  
  
4.  Repeat this procedure for the **ID_CONTEXT_HELP** command.  
  
     This maps to the help mode toolbar button, described later in this lesson, in [Copying the Help Mode Toolbar Button](../vs140/-PAVE-OVER--Copying-the-Help-Mode-Toolbar-Button.md).  
  
5.  Close both accelerator editor windows.  
  
## See Also  
 [<PAVE OVER\> Copying Help-Specific Resources to Your Project](../vs140/-PAVE-OVER--Copying-Help-Specific-Resources-to-Your-Project.md)