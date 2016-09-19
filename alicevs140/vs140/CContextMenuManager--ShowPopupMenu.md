---
title: "CContextMenuManager::ShowPopupMenu"
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
ms.assetid: e7de5697-27a6-45f3-9fc5-11057ad7e91c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::ShowPopupMenu
Displays the specified shortcut menu.  
  
## Syntax  
  
```  
virtual BOOL ShowPopupMenu(  
   UINT uiMenuResId,  
   int x,  
   int y,  
   CWnd* pWndOwner,  
   BOOL bOwnMessage = FALSE,  
   BOOL bRightAlign = FALSE  
);  
  
virtual CMFCPopupMenu* ShowPopupMenu(  
   HMENU hmenuPopup,  
   int x,  
   int y,  
   CWnd* pWndOwner,  
   BOOL bOwnMessage = FALSE,  
   BOOL bAutoDestroy = TRUE,  
   BOOL bRightAlign = FALSE  
);  
```  
  
#### Parameters  
 [in] `uiMenuResId`  
 The resource ID of the menu that this method will display.  
  
 [in] `x`  
 The horizontal offset for the shortcut menu in client coordinates.  
  
 [in] `y`  
 The vertical offset for the shortcut menu in client coordinates  
  
 [in] `pWndOwner`  
 A pointer to the parent window of the shortcut menu.  
  
 [in] `bOwnMessage`  
 A Boolean parameter that indicates how messages are routed. If `bOwnMessage` is `FALSE`, standard MFC routing is used. Otherwise, `pWndOwner` receives the messages.  
  
 [in] `hmenuPopup`  
 The handle of the menu that this method will display.  
  
 [in] `bAutoDestroy`  
 A Boolean parameter that indicates whether the menu will be automatically destroyed.  
  
 [in] `bRightAlign`  
 A Boolean parameter that indicates how the menu items are aligned. If `bRightAlign` is `TRUE`, the menu is right-aligned for right-to-left reading order.  
  
## Return Value  
 The first method overload returns nonzero if the method shows the menu successfully; otherwise 0. The second method overload returns a pointer to [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) if the shortcut menu displays correctly; otherwise `NULL`.  
  
## Remarks  
 This method resembles the method [CContextMenuManager::TrackPopupMenu](../vs140/CContextMenuManager--TrackPopupMenu.md) in that both methods display a shortcut menu. However, `TrackPopupMenu` returns the index of the selected menu command.  
  
 If the parameter `bAutoDestroy` is `FALSE`, you must manually call the inherited `DestroyMenu` method to release memory resources. The default implementation of `ShowPopupMenu` does not use the parameter `bAutoDestroy`. It is provided for future use or for custom classes derived from the [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md).  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CContextMenuManager::TrackPopupMenu](../vs140/CContextMenuManager--TrackPopupMenu.md)