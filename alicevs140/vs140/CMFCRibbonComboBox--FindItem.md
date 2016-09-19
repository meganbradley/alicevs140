---
title: "CMFCRibbonComboBox::FindItem"
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
ms.assetid: 320b16e2-807a-4028-9e16-a590be2c97b1
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonComboBox::FindItem
Returns the index of the first item in the list box that matches a specified string.  
  
## Syntax  
  
```  
int FindItem(  
   LPCTSTR lpszText   
) const;  
```  
  
#### Parameters  
 [in] `lpszText`  
 The string of an item in the list box.  
  
## Return Value  
 The zero-based index of the item; or -1 if the item is not found.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncombobox.h  
  
## See Also  
 [CMFCRibbonComboBox Class](../vs140/CMFCRibbonComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)