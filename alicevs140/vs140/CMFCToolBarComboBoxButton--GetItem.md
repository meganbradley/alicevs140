---
title: "CMFCToolBarComboBoxButton::GetItem"
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
ms.assetid: f13c4658-2fdf-4298-9c87-44dead707183
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::GetItem
Returns the string associated with an item at a specified index in the list box.  
  
## Syntax  
  
```  
LPCTSTR GetItem(  
   int iIndex=-1   
) const;  
```  
  
#### Parameters  
 [in] `iIndex`  
 Zero-based index of an item in the list box.  
  
## Return Value  
 A pointer to the string that is associated with the item; otherwise, `NULL` if the index parameter is invalid, or if the index parameter is -1 and there is no selected item in the combo box.  
  
## Remarks  
 An index parameter of -1 returns the string of the item that is currently selected.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)