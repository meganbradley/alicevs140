---
title: "CMDIFrameWndEx::EnablePaneMenu"
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
ms.topic: reference
ms.assetid: 4ee54bc3-6cd8-4d79-bfd5-6597aaadf995
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::EnablePaneMenu
Enables or disables automatic creation and management of the pop-up pane menu, which displays a list of application panes.  
  
## Syntax  
  
```  
void EnablePaneMenu(  
   BOOL bEnable,  
   UINT uiCustomizeCmd,  
   const CString& strCustomizeLabel,  
   UINT uiViewToolbarsMenuEntryID,  
   BOOL bContextMenuShowsToolbarsOnly=FALSE,  
   BOOL bViewMenuShowsToolbarsOnly=FALSE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 If `TRUE`, automatic handling of the pane menu is enabled; if `FALSE`, automatic handling is disabled.  
  
 [in] `uiCustomizeCmd`  
 Command ID of the **Customize** menu item. This menu item is usually added to the end of the list of panes.  
  
 [in] `strCustomizeLabel`  
 The text to be displayed for the **Customize** menu item (for localization).  
  
 [in] `uiViewToolbarsMenuEntryID`  
 Specifies the ID of a toolbar menu item that opens the pane menu. Usually this is the **Toolbars** submenu of the **View** menu.  
  
 [in] `bContextMenuShowsToolbarsOnly`  
 If `TRUE`, the pane menu displays only a list of toolbars. If `FALSE`, the menu displays a list of toolbars and docking bars.  
  
 [in] `bViewMenuShowsToolbarsOnly`  
 If `TRUE`, the pane menu displays only a list of toolbars. If `FALSE`, the menu displays a list of toolbars and docking bars.  
  
## Remarks  
 The pop-up pane menu displays the list of the application's panes and lets the user show or hide individual panes.  
  
## Example  
 The following example shows how `EnablePaneMenu` is used in the [VisualStudioDemo Sample: MFC Visual Studio Application](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#9](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#9)]  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)