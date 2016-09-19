---
title: "CMFCPopupMenu::GetSelItem"
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
ms.assetid: cbc7a6de-781e-44b9-a808-bfff9c726c5b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetSelItem
Returns a pointer to the currently selected menu command.  
  
## Syntax  
  
```  
CMFCToolBarMenuButton* GetSelItem();  
```  
  
## Return Value  
 A pointer to the currently selected menu command; `NULL` if no item is selected.  
  
## Remarks  
 The menu commands on a pop-up menu are represented by the [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md), or a class derived from `CMFCToolBarMenuButton`.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)