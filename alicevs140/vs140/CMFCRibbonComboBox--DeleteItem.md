---
title: "CMFCRibbonComboBox::DeleteItem"
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
ms.assetid: d23b1c68-2bb4-4b74-b1ea-a8caa0c58d0c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonComboBox::DeleteItem
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
 The string of the item to be deleted. If there are multiple items with the same string, the first item is deleted.  
  
## Return Value  
 `TRUE` if the specified item has been deleted; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncombobox.h  
  
## See Also  
 [CMFCRibbonComboBox Class](../vs140/CMFCRibbonComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)