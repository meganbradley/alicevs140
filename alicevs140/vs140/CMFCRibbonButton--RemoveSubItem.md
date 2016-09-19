---
title: "CMFCRibbonButton::RemoveSubItem"
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
ms.assetid: f4bc97b7-663b-4db6-8eff-3d0510a352e1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButton::RemoveSubItem
Removes a menu item from the pop-up menu.  
  
## Syntax  
  
```  
BOOL RemoveSubItem(  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the zero-based index of the menu item that you want to remove.  
  
## Return Value  
 `TRUE` if the specified item has been removed successfully; otherwise `FALSE` if `nIndex` is negative or exceeds the number of menu items in the pop-up menu.  
  
## Requirements  
 **Header:** afxribbonbutton.h  
  
## See Also  
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)