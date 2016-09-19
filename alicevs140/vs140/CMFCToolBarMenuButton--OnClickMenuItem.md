---
title: "CMFCToolBarMenuButton::OnClickMenuItem"
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
ms.assetid: 06fcb314-b745-4724-9a74-a76cce4dd292
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::OnClickMenuItem
Called by the framework when the user selects an item in the drop-down menu.  
  
## Syntax  
  
```  
virtual BOOL OnClickMenuItem();  
```  
  
## Return Value  
 `FALSE` if the framework should continue the default menu item processing; otherwise `TRUE`. The default implementation always returns `FALSE`.  
  
## Remarks  
 When the user clicks a menu item, the framework executes a command that is associated with that item.  
  
 To customize the menu item processing, override `OnClickMenuItem` in a class derived from `CMFCToolBarMenuButton` class. You must also override [CFrameWndEx::OnShowPopupMenu](../vs140/CFrameWndEx--OnShowPopupMenu.md) and replace the menu buttons that require special processing with instances of the derived class.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)