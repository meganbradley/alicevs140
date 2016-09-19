---
title: "CMFCVisualManager::IsOfficeXPStyleMenus"
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
ms.assetid: c3e5dc90-d489-4a76-b06a-7428a29846fa
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::IsOfficeXPStyleMenus
Indicates whether the visual manager implements Office XP-style menus.  
  
## Syntax  
  
```  
virtual BOOL IsOfficeXPStyleMenus() const;  
```  
  
## Return Value  
 Nonzero if the visual manager displays Office XP-style menus; otherwise 0.  
  
## Remarks  
 The [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md) calls this method when it has to draw the menu and shadow. By default, this method returns `FALSE`. If you want to use pop-up menus similar to the pop-up menus in Office XP, override this method in a custom visual manager and return `TRUE`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)