---
title: "CMFCPopupMenu::RemoveItem"
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
ms.assetid: 2f5b7981-15f6-4270-ba23-e4b39b5fdf03
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::RemoveItem
Removes the specified item from the pop-up menu.  
  
## Syntax  
  
```  
BOOL RemoveItem(  
   int iIndex   
);  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of the item to delete.  
  
## Return Value  
 `TRUE` if the method is successful; otherwise `FALSE`.  
  
## Remarks  
 This method automatically arranges any separators that are affected by the removal of an item. For more information about how the framework rearranges separators, see [CMFCToolBar::RemoveButton](../vs140/CMFCToolBar--RemoveButton.md).  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)