---
title: "Updating the Text of a Status-Bar Pane"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4984a3f4-9905-4d8c-a927-dca19781053b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Updating the Text of a Status-Bar Pane
This article explains how to change the text that appears in an MFC status bar pane. A status bar — a window object of class [CStatusBar](../vs140/CStatusBar-Class.md) — contains several "panes." Each pane is a rectangular area of the status bar that you can use to display information. For example, many applications display the status of the CAPS LOCK, NUM LOCK, and other keys in the rightmost panes. Applications also often display informative text in the leftmost pane (pane 0), sometimes called the "message pane." For example, the default MFC status bar uses the message pane to display a string explaining the currently selected menu item or toolbar button. The figure in [Status Bars](../vs140/Status-Bar-Implementation-in-MFC.md) shows a status bar from an Application Wizard-created MFC application.  
  
 By default, MFC does not enable a `CStatusBar` pane when it creates the pane. To activate a pane, you must use the `ON_UPDATE_COMMAND_UI` macro for each pane on the status bar and update the panes. Because panes do not send **WM_COMMAND** messages (they aren't like toolbar buttons), you must type the code manually.  
  
 For example, suppose one pane has `ID_INDICATOR_PAGE` as its command identifier and that it contains the current page number in a document. The following procedure describes how to create a new pane in the status bar.  
  
### To make a new pane  
  
1.  Define the pane's command ID.  
  
     On the **View** menu, click **Resource View**. Right-click the project resource and click **Resource Symbols**. In the Resource Symbols dialog box, click `New`. Type a command ID name: for example, `ID_INDICATOR_PAGE`. Specify a value for the ID, or accept the value suggested by the Resource Symbols dialog box. For example, for `ID_INDICATOR_PAGE`, accept the default value. Close the Resource Symbols dialog box.  
  
2.  Define a default string to display in the pane.  
  
     With Resource View open, double-click **String Table** in the window that lists resource types for your application. With the **String Table** editor open, choose **New String** from the **Insert** menu. In the String Properties window, select your pane's command ID (for example, `ID_INDICATOR_PAGE`) and type a default string value, such as "Page   ". Close the string editor. (You need a default string to avoid a compiler error.)  
  
3.  Add the pane to the **indicators** array.  
  
     In file MAINFRM.CPP, locate the **indicators** array. This array lists command IDs for all of the status bar's indicators, in order from left to right. At the appropriate point in the array, enter your pane's command ID, as shown here for `ID_INDICATOR_PAGE`:  
  
     [!CODE [NVC_MFCDocView#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#10)]  
  
 The recommended way to display text in a pane is to call the **SetText** member function of class `CCmdUI` in an update handler function for the pane. For example, you might want to set up an integer variable `m_nPage` that contains the current page number and use **SetText** to set the pane's text to a string version of that number.  
  
> [!NOTE]
>  The **SetText** approach is recommended. It is possible to perform this task at a slightly lower level by calling the `CStatusBar` member function `SetPaneText`. Even so, you still need an update handler. Without such a handler for the pane, MFC automatically disables the pane, erasing its content.  
  
 The following procedure shows how to use an update handler function to display text in a pane.  
  
#### To make a pane display text  
  
1.  Add a command update handler for the command.  
  
     Manually add a prototype for the handler, as shown here for `ID_INDICATOR_PAGE` (in MAINFRM.H):  
  
     [!CODE [NVC_MFCDocView#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#11)]  
  
2.  In the appropriate .CPP file, add the handler's definition, as shown here for `ID_INDICATOR_PAGE` (in MAINFRM.CPP):  
  
     [!CODE [NVC_MFCDocView#12](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#12)]  
  
     The last three lines of this handler are the code that displays your text.  
  
3.  In the appropriate message map, add the `ON_UPDATE_COMMAND_UI` macro, as shown here for `ID_INDICATOR_PAGE` (in MAINFRM.CPP):  
  
     [!CODE [NVC_MFCDocView#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#13)]  
  
 Once you define the value of the `m_nPage` member variable (of class `CMainFrame`), this technique causes the page number to appear in the pane during idle processing in the same manner that the application updates other indicators. If `m_nPage` changes, the display changes during the next idle loop.  
  
### What do you want to know more about?  
  
-   [Updating user-interface objects (how to update toolbar buttons and menu items as program conditions change)](../vs140/How-to--Update-User-Interface-Objects.md)  
  
## See Also  
 [Status Bar Implementation in MFC](../vs140/Status-Bar-Implementation-in-MFC.md)   
 [CStatusBar Class](../vs140/CStatusBar-Class.md)