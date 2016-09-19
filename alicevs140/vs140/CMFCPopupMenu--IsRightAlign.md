---
title: "CMFCPopupMenu::IsRightAlign"
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
ms.assetid: d8b47cbf-f468-42d7-a14d-dd129176097d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::IsRightAlign
Indicates whether the menu is right-aligned or left-aligned.  
  
## Syntax  
  
```  
BOOL IsRightAlign() const;  
```  
  
## Return Value  
 `TRUE` if the menu is right-aligned; `FALSE` if the menu left-aligned.  
  
## Remarks  
 You can use [CMFCPopupMenu::SetRightAlign](../vs140/CMFCPopupMenu--SetRightAlign.md) to set the menu alignment. By default, pop-up menus use left-alignment.  
  
 Menu alignment is not a global setting and can vary between pop-up menus.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenu::SetRightAlign](../vs140/CMFCPopupMenu--SetRightAlign.md)