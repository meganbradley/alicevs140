---
title: "CWinAppEx::ShowPopupMenu"
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
ms.assetid: da7ff5b2-bdd7-4743-a584-67acb9f8c7d8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::ShowPopupMenu
Displays a popup menu.  
  
## Syntax  
  
```  
virtual BOOL ShowPopupMenu(  
   UINT uiMenuResId,  
   const CPoint& point,  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 [in] `uiMenuResId`  
 A menu resource ID.  
  
 [in] `point`  
 A [CPoint](../vs140/CPoint-Class.md) that specifies the position of the menu in screen coordinates.  
  
 [in] `pWnd`  
 A pointer to the window that owns the popup menu.  
  
## Return Value  
 Nonzero if the popup menu is displayed successfully; 0 otherwise.  
  
## Remarks  
 This method displays the menu associated with `uiMenuResId`.  
  
 To support popup menus, you must have a [CContextMenuManager](../vs140/CContextMenuManager-Class.md) object. If you have not initialized the `CContextMenuManager` object, `ShowPopupMenu` will fail.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)