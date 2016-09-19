---
title: "CMenu::GetMenuItemID"
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
ms.assetid: 9a984cc6-8868-4585-ae46-ec3add80de1b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::GetMenuItemID
Obtains the menu-item identifier for a menu item located at the position defined by `nPos`.  
  
## Syntax  
  
```  
  
      UINT GetMenuItemID(  
   int nPos   
) const;  
```  
  
#### Parameters  
 `nPos`  
 Specifies the position (zero-based) of the menu item whose ID is being retrieved.  
  
## Return Value  
 The item ID for the specified item in a pop-up menu if the function is successful. If the specified item is a pop-up menu (as opposed to an item within the pop-up menu), the return value is –1. If `nPos` corresponds to a **SEPARATOR** menu item, the return value is 0.  
  
## Example  
 See the example for [CMenu::InsertMenu](../vs140/CMenu--InsertMenu.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::GetMenu](../vs140/CWnd--GetMenu.md)   
 [CMenu::GetMenuItemCount](../vs140/CMenu--GetMenuItemCount.md)   
 [CMenu::GetSubMenu](../vs140/CMenu--GetSubMenu.md)   
 [GetMenuItemID](http://msdn.microsoft.com/library/windows/desktop/ms647979)