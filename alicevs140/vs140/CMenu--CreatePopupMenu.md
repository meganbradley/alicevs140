---
title: "CMenu::CreatePopupMenu"
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
ms.assetid: 09a587e0-698f-4d44-9cac-74bd9556531c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::CreatePopupMenu
Creates a pop-up menu and attaches it to the `CMenu` object.  
  
## Syntax  
  
```  
  
BOOL CreatePopupMenu( );  
```  
  
## Return Value  
 Nonzero if the pop-up menu was successfully created; otherwise 0.  
  
## Remarks  
 The menu is initially empty. Menu items can be added by using the `AppendMenu` or `InsertMenu` member function. The application can add the pop-up menu to an existing menu or pop-up menu. The `TrackPopupMenu` member function may be used to display this menu as a floating pop-up menu and to track selections on the pop-up menu.  
  
 If the menu is assigned to a window, it is automatically destroyed when the window is destroyed. If the menu is added to an existing menu, it is automatically destroyed when that menu is destroyed.  
  
 Before exiting, an application must free system resources associated with a pop-up menu if the menu is not assigned to a window. An application frees a menu by calling the [DestroyMenu](../vs140/CMenu--DestroyMenu.md) member function.  
  
## Example  
 See the example for [CMenu::CreateMenu](../vs140/CMenu--CreateMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMenu::CreateMenu](../vs140/CMenu--CreateMenu.md)   
 [CMenu::InsertMenu](../vs140/CMenu--InsertMenu.md)   
 [CWnd::SetMenu](../vs140/CWnd--SetMenu.md)   
 [CMenu::TrackPopupMenu](../vs140/CMenu--TrackPopupMenu.md)   
 [CreatePopupMenu](http://msdn.microsoft.com/library/windows/desktop/ms647626)   
 [CMenu::AppendMenu](../vs140/CMenu--AppendMenu.md)