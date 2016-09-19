---
title: "CMFCPopupMenu::SetForceMenuFocus"
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
ms.assetid: 35336d98-b0b7-4855-9334-73df09a6254c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::SetForceMenuFocus
Forces the input focus to return to the menu bar when a pop-up menu is displayed.  
  
## Syntax  
  
```  
static void SetForceMenuFocus(  
   BOOL bValue   
);  
```  
  
#### Parameters  
 [in] `bValue`  
 `TRUE` if you want the framework to force the input focus to the menu bar when a pop-up menu is displayed. `FALSE` if you want the pop-up menu to retain the focus.  
  
## Remarks  
 This method sets a flag that is global for all pop-up menus in the application. By default, this feature is not enabled.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)