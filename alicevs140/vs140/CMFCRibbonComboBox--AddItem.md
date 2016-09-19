---
title: "CMFCRibbonComboBox::AddItem"
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
ms.assetid: eeaf78bf-c556-49e3-8565-7d9c58e646bf
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonComboBox::AddItem
Appends a unique item to the list box.  
  
## Syntax  
  
```  
virtual INT_PTR AddItem(  
   LPCTSTR lpszItem,  
   DWORD_PTR dwData=0   
);  
```  
  
#### Parameters  
 [in] `lpszItem`  
 The string of the item to add.  
  
 [in] `dwData`  
 The data associated with the item to add.  
  
## Return Value  
 The zero-based index of the appended item.  
  
## Requirements  
 **Header:** afxribboncombobox.h  
  
## See Also  
 [CMFCRibbonComboBox Class](../vs140/CMFCRibbonComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)