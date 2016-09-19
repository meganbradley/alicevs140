---
title: "CMFCToolBarComboBoxButton::AddSortedItem"
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
ms.assetid: 71f1f11c-1e71-417b-a5bc-1ab7efda8989
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::AddSortedItem
Adds an item to the list box in the order that is defined by the [Compare](../vs140/CMFCToolBarComboBoxButton--Compare.md) method.  
  
## Syntax  
  
```  
virtual INT_PTR AddSortedItem(  
   LPCTSTR lpszItem,  
   DWORD_PTR dwData=0   
);  
```  
  
#### Parameters  
 [in] `lpszItem`  
 The text of the item to add to the list box.  
  
 [in] `dwData`  
 The data associated with the item to add to the list box.  
  
## Return Value  
 Index of the item that was added to the list box.  
  
## Remarks  
 Use this function to add items to the list box in a specific order.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarComboBoxButton::Compare](../vs140/CMFCToolBarComboBoxButton--Compare.md)