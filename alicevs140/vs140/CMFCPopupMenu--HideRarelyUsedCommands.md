---
title: "CMFCPopupMenu::HideRarelyUsedCommands"
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
ms.assetid: 414df65d-8a9c-4c33-8f7c-6285fce9b53d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::HideRarelyUsedCommands
Indicates whether the pop-up menu can hide rarely used commands.  
  
## Syntax  
  
```  
BOOL HideRarelyUsedCommands() const;  
```  
  
## Return Value  
 `TRUE` if the pop-up menu can hide the rarely used commands; otherwise `FALSE`.  
  
## Remarks  
 This method specifies only whether a pop-up menu can hide rarely used commands, not if that configuration is enabled. A pop-up menu can hide rarely used commands if it has a parent button and the parent window is derived from the [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md). Use [CMFCMenuBar::SetRecentlyUsedMenus](../vs140/CMFCMenuBar--SetRecentlyUsedMenus.md) to enable this feature and [CMFCMenuBar::IsRecentlyUsedMenus](../vs140/CMFCMenuBar--IsRecentlyUsedMenus.md) to determine if this feature is currently enabled. You must call both of these methods for the parent window.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::SetRecentlyUsedMenus](../vs140/CMFCMenuBar--SetRecentlyUsedMenus.md)   
 [CMFCMenuBar::IsRecentlyUsedMenus](../vs140/CMFCMenuBar--IsRecentlyUsedMenus.md)