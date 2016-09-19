---
title: "CMFCToolBarMenuButton::GetPopupMenu"
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
ms.assetid: acb5fed8-dd1c-4569-a8d0-9121f6f0fc79
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::GetPopupMenu
Returns a pointer to the [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) object that represents the drop-down menu of the button.  
  
## Syntax  
  
```  
CMFCPopupMenu* GetPopupMenu() const;  
```  
  
## Return Value  
 A pointer to a [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) object that was created when the framework drew the submenu of the toolbar menu button; `NULL` if no submenu is displayed.  
  
## Remarks  
 When a toolbar menu button displays a drop-down menu, the button creates a [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) object to represent the menu. Call this method to obtain a pointer to the `CMFCPopupMenu` object. You should not store the returned pointer, because it is temporary and becomes invalid when the user closes the drop-down menu.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)