---
title: "CMFCRibbonComboBox::GetItem"
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
ms.assetid: 9fcba287-e9a1-46cb-beeb-2b77d9a701bf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonComboBox::GetItem
Returns the string associated with an item at a specified index in the list box.  
  
## Syntax  
  
```  
LPCTSTR GetItem(  
   int iIndex   
) const;  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of an item in the list box.  
  
## Return Value  
 A pointer to the string that is associated with the item; otherwise, `NULL` if the index parameter is invalid, or if the index parameter is -1 and there is no item selected in the combo box.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncombobox.h  
  
## See Also  
 [CMFCRibbonComboBox Class](../vs140/CMFCRibbonComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)