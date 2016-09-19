---
title: "CMFCPopupMenu::IsQuickCustomize"
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
ms.assetid: 0a8dc519-6d01-43de-9e33-68d6d7d7e22a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::IsQuickCustomize
Determines whether the associated [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md) is in QuickCustomize mode.  
  
## Syntax  
  
```  
BOOL IsQuickCustomize();  
```  
  
## Return Value  
 `TRUE` if the associated menu button is in QuickCustomize mode; otherwise `FALSE`. This method will also return `FALSE` if the pop-up menu is not associated with a `CMFCToolBarMenuButton`.  
  
## Remarks  
 In QuickCustomize mode the user selects a button on a toolbar to customize the button directly.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)