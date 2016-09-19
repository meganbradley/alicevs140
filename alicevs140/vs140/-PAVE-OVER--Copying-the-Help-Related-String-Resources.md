---
title: "&lt;PAVE OVER&gt; Copying the Help-Related String Resources"
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
ms.assetid: ba258e60-ca59-4c1c-aae9-1db1530f5f45
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;PAVE OVER&gt; Copying the Help-Related String Resources
In this procedure you copy the command IDs for Help-related menu items.  
  
### To edit Help-related string resources  
  
1.  Open the String Table resource for both your application and HasHelp resizing both editor windows, as described in [Copying the Help Menu Resources](../vs140/-PAVE-OVER--Copying-the-Help-Menu-Resources.md), so they do not overlap.  
  
2.  Locate the **AFX_IDS_IDLEMESSAGE** string in both tables, noting the difference in the captions.  
  
     For an application without help, the MFC Application Wizard defines the default status-bar prompt to be `Ready`. This is the string displayed in the status bar when no other command prompt is being displayed.  
  
3.  Select the **Caption** column for **AFX_IDS_IDLEMESSAGE** in your project's string table, and edit the caption so that it matches the HasHelp version of this string resource: `For Help, press F1`.  
  
4.  Next, copy the following strings from the HasHelp String Table to your project's String Table:  
  
    -   `AFX_IDS_HELPMODEMESSAGE` (Displays in the status bar while the application is in help mode.)  
  
    -   `ID_CONTEXT_HELP` (Displays when the mouse pauses over the help mode toolbar button.`)`  
  
    -   `ID_HELP` (Called when the user presses F1.)  
  
    -   `ID_HELP_FINDER` (Displays for the **Help Topics** command on the **Help** menu.)  
  
     The copying procedure is similar to the procedures for copying menus and accelerators. To copy several contiguous strings, hold the SHIFT key down while selecting the strings. Then hold the CTRL key down while dragging the selected strings to the new window.  
  
5.  Close the String Table resources.  
  
## See Also  
 [<PAVE OVER\> Copying Help-Specific Resources to Your Project](../vs140/-PAVE-OVER--Copying-Help-Specific-Resources-to-Your-Project.md)