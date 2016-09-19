---
title: "CMFCToolBarMenuButton::CreatePopupMenu"
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
ms.assetid: 883ce342-07e3-41c0-90f5-2258b53e1d98
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::CreatePopupMenu
Creates a `CMFCPopupMenu` object to display the toolbar menu.  
  
## Syntax  
  
```  
virtual CMFCPopupMenu* CreatePopupMenu();  
```  
  
## Return Value  
 A pointer to a `CMFCPopupMenu` object that displays the drop-down menu associated with the toolbar menu button.  
  
## Remarks  
 This method is called by the framework to prepare the display of the drop-down menu associated with the button.  
  
 The default implementation just constructs and returns a new `CMFCPopupMenu` object. Override this method if you want to use a derived type of [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) or to perform additional initialization.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)