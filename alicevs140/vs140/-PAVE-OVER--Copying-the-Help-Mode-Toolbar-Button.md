---
title: "&lt;PAVE OVER&gt; Copying the Help Mode Toolbar Button"
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
ms.assetid: dd76857d-d73e-4f7e-a92c-402b1123a7e2
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Copying the Help Mode Toolbar Button
When you generate context-sensitive Help from the MFC Application Wizard, a button is created on the toolbar which, when selected, places the application in Help mode, just as pressing SHIFT+F1 does.  
  
 In this procedure you'll copy the Help mode button to your project's toolbar resource from the HasHelp project toolbar resource, simply by dragging it.  
  
### To copy the Help mode toolbar button  
  
1.  Open your project's toolbar resource and HasHelp's toolbar resource, resizing both editor windows, as described in [Copying the Help Menu Resources](../vs140/-PAVE-OVER--Copying-the-Help-Menu-Resources.md), so they do not overlap and so you can see both subject toolbars.  
  
2.  Press CTRL and drag the Help mode button from HasHelp's toolbar onto your project's toolbar.  
  
3.  Save the resource file for your project (.rc file), and close the HasHelp resource file.  
  
## See Also  
 [<PAVE OVER\> Copying Help-Specific Resources to Your Project](../vs140/-PAVE-OVER--Copying-Help-Specific-Resources-to-Your-Project.md)