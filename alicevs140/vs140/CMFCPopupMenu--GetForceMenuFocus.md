---
title: "CMFCPopupMenu::GetForceMenuFocus"
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
ms.assetid: 40e3387d-60a4-4012-af47-c03c6ce0705b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetForceMenuFocus
Indicates whether the focus is returned to the menu bar when a pop-up menu is displayed.  
  
## Syntax  
  
```  
static BOOL GetForceMenuFocus();  
```  
  
## Return Value  
 `TRUE` if the input focus is returned to the menu bar when a pop-up menu is displayed; `FALSE` if the pop-up menu retains the focus.  
  
## Remarks  
 By default, your application does not return focus to the menu bar. To change this setting, use [CMFCPopupMenu::SetForceMenuFocus](../vs140/CMFCPopupMenu--SetForceMenuFocus.md).  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenu::SetForceMenuFocus](../vs140/CMFCPopupMenu--SetForceMenuFocus.md)