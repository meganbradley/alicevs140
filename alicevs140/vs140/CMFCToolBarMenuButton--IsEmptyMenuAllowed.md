---
title: "CMFCToolBarMenuButton::IsEmptyMenuAllowed"
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
ms.assetid: b98a6c5c-3c8b-4c35-a51d-81dfa76f7726
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::IsEmptyMenuAllowed
Specifies whether menu items shows empty submenus.  
  
## Syntax  
  
```  
virtual BOOL IsEmptyMenuAllowed() const;  
```  
  
## Return Value  
 `TRUE` if the framework opens a submenu from the currently selected menu item even when the submenu is empty; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method when a user tries to open the submenu from the currently selected menu item. If the submenu is empty and `IsEmptyMenuAllowed` returns `FALSE`, the submenu will not open.  
  
 The default implementation returns `FALSE`. Override this method to customize this behavior.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)