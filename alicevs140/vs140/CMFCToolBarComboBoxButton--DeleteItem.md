---
title: "CMFCToolBarComboBoxButton::DeleteItem"
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
ms.assetid: 8a790f08-84ba-4180-8bb9-40a5957b2bfa
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::DeleteItem
Deletes a specified item from the list box.  
  
## Syntax  
  
```  
BOOL DeleteItem(  
   int iIndex   
);  
BOOL DeleteItem(  
   DWORD_PTR dwData   
);  
BOOL DeleteItem(  
   LPCTSTR lpszText   
);  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of the item to be deleted.  
  
 [in] `dwData`  
 The data associated with the item to be deleted.  
  
 [in] `lpszText`  
 The text of the item to be deleted. If there are multiple items with the same text, the first item is deleted.  
  
## Return Value  
 `TRUE` if the item was located and successfully deleted; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)