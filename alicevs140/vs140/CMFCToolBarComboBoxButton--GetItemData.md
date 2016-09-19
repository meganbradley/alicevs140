---
title: "CMFCToolBarComboBoxButton::GetItemData"
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
ms.assetid: c1cb8b78-84d4-4a8f-8605-cf59056e4451
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::GetItemData
Returns the data associated with an item at a specific index in the list box.  
  
## Syntax  
  
```  
DWORD_PTR GetItemData(  
   int iIndex=-1   
) const;  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of an item in the list box.  
  
## Return Value  
 The data associated with the item; or 0 if the item does not exist.  
  
## Remarks  
 An index parameter of -1 returns the data associated with the currently selected item.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)