---
title: "Testing a Dialog Box"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 45034ee9-c554-4f4b-8c46-6ddefdee8951
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Testing a Dialog Box
When you're designing a dialog box, you can simulate and test its run-time behavior without compiling your program. In this mode, you can:  
  
-   Type text, select from combo-box lists, turn options on or off, and choose commands.  
  
-   Test the tab order.  
  
-   Test the grouping of controls such as radio buttons and check boxes.  
  
-   Test the keyboard shortcuts for controls in the dialog box.  
  
    > [!NOTE]
    >  Connections to dialog box code made by using wizards are not included in the simulation.  
  
 When you test a dialog box, it typically displays at a location that's relative to the main program window. If you've set the dialog box's Absolute Align property to True, the dialog box displays at a position that's relative to the upper-left corner of the screen.  
  
### To test a dialog box  
  
1.  When the Dialog editor is the active window, on the menu bar, choose **Format**, **Test Dialog**.  
  
2.  To end the simulation, press Esc, or just choose the **Close** button in the dialog box you are testing.  
  
 For information about how to add resources to managed projects, see [Resources in Applications](assetId:///8ad495d4-2941-40cf-bf64-e82e85825890).  
  
 Requirements  
  
 Win32  
  
## See Also  
 [Controls in Dialog Boxes](../vs140/Controls-in-Dialog-Boxes.md)   
 [Dialog Editor](../vs140/Dialog-Editor.md)   
 [Showing or Hiding the Dialog Editor Toolbar](../vs140/Showing-or-Hiding-the-Dialog-Editor-Toolbar.md)