---
title: "CMFCPopupMenu::GetMenuItem"
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
ms.assetid: 7d3ba6ca-7900-4dce-a196-d4476b5b1b8f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetMenuItem
Returns a pointer to the menu item at the specified index.  
  
## Syntax  
  
```  
CMFCToolBarMenuButton* GetMenuItem(  
   int iIndex   
) const;  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of a menu item.  
  
## Return Value  
 A pointer to a menu item. `NULL` if the index is invalid.  
  
## Remarks  
 Menu items are represented by the [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md). When you call this method, it returns a pointer to the appropriate `CMFCToolBarMenuButton`.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)