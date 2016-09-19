---
title: "CMenu::GetSubMenu"
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
ms.assetid: 181aaf3f-3659-44f2-ae94-0e0fafe86832
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::GetSubMenu
Retrieves the `CMenu` object of a pop-up menu.  
  
## Syntax  
  
```  
  
      CMenu* GetSubMenu(  
   int nPos   
) const;  
```  
  
#### Parameters  
 `nPos`  
 Specifies the position of the pop-up menu contained in the menu. Position values start at 0 for the first menu item. The pop-up menu's identifier cannot be used in this function.  
  
## Return Value  
 A pointer to a `CMenu` object whose `m_hMenu` member contains a handle to the pop-up menu if a pop-up menu exists at the given position; otherwise **NULL**. If a `CMenu` object does not exist, then a temporary one is created. The `CMenu` pointer returned should not be stored.  
  
## Example  
 See the example for [CMenu::TrackPopupMenu](../vs140/CMenu--TrackPopupMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetMenu](../vs140/CWnd--GetMenu.md)   
 [CMenu::GetMenuItemID](../vs140/CMenu--GetMenuItemID.md)   
 [GetSubMenu](http://msdn.microsoft.com/library/windows/desktop/ms647984)