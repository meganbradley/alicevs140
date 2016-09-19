---
title: "CMFCToolBarComboBoxButton::SelectItem"
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
ms.assetid: 6935ceb0-003d-4160-a389-b875a78d92e4
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::SelectItem
Selects an item in the list box.  
  
## Syntax  
  
```  
BOOL SelectItem(  
   int iIndex,  
   BOOL bNotify=TRUE   
);  
BOOL SelectItem(  
   DWORD_PTR dwData   
);  
BOOL SelectItem(  
   LPCTSTR lpszText   
);  
```  
  
#### Parameters  
 [in] `iIndex`  
 The zero-based index of an item in the list box.  
  
 [in] `bNotify`  
 `TRUE` to notify the combo box button of the selection; otherwise `FALSE`.  
  
 [in] `dwData`  
 The data associated with an item in the list box.  
  
 [in] `lpszText`  
 The text of an item in the list box.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)