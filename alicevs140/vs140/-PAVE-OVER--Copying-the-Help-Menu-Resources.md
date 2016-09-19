---
title: "&lt;PAVE OVER&gt; Copying the Help Menu Resources"
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
ms.assetid: 208f3739-4e13-4c47-9fad-c8ee318c078b
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Copying the Help Menu Resources
First, copy Help-related menu resources from the HasHelp project to your project.  
  
### To copy Help menu resources to your project  
  
1.  Open your project's .rc file and the HasHelp.rc, which are located in their respective project directories. These files display the contents of the **Resource View** panes for both your project and HasHelp.  
  
2.  Select **IDR_MAINFRAME** from the **Menu** folder from both resource files.  
  
     Right-click at the top of the first **IDR_MAINFRAME - Menu** window and select **New Horizontal Tab Group**. This will allow you to view both menu windows.  
  
3.  Click the **Help Topics** menu item in the HasHelp **Help** menu. Then hold down the SHIFT key while you click the separator below the **Help Topics** item. Release the SHIFT key.  
  
     This selects the menu item and separator.  
  
4.  Hold down the CTRL key and use the mouse to drag the highlighted menu items to the **Help** menu in your project's .rc file, above the **About** menu item. Release the mouse button and the CTRL key.  
  
     This copies the menu item and the separator to your project.  
  
5.  Close the two **IDR_MAINFRAME** menu-editing windows.  
  
6.  Repeat steps 3 through 6, for the **Help** menu using the application-specific menu resource, `IDR_`*your_proj*`TYPE`.  
  
## See Also  
 [<PAVE OVER\> Copying Help-Specific Resources to Your Project](../vs140/-PAVE-OVER--Copying-Help-Specific-Resources-to-Your-Project.md)