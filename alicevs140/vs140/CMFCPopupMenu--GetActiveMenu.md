---
title: "CMFCPopupMenu::GetActiveMenu"
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
ms.assetid: d2a834e9-96aa-4241-94aa-6007bd1191e6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetActiveMenu
Returns the currently active menu.  
  
## Syntax  
  
```  
static CMFCPopupMenu* GetActiveMenu();  
```  
  
## Return Value  
 A pointer to the active pop-up menu, or NULL if no pop-up menu is currently active.  
  
## Remarks  
 Each application can have at most one active pop-up menu.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)