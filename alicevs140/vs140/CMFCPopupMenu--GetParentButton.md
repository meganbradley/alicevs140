---
title: "CMFCPopupMenu::GetParentButton"
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
ms.assetid: 9ba01797-f020-4968-bc6a-417102e5b8d7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::GetParentButton
Returns a pointer to the parent toolbar button.  
  
## Syntax  
  
```  
CMFCToolBarMenuButton* GetParentButton() const;  
```  
  
## Return Value  
 A pointer to the parent toolbar button. `NULL` if the pop-up menu has no parent toolbar button.  
  
## Remarks  
 A [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) can be associated with a button on the menu. In this scenario, the pop-up menu appears when a user selects the parent toolbar button.  
  
 If the pop-up menu is a shortcut menu, it will have no parent toolbar button.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)