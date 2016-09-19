---
title: "CMFCToolBarComboBoxButton::GetItemDataAll"
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
ms.assetid: 2c785e1c-6fe9-4bf8-a5f0-60fde13968fa
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::GetItemDataAll
Returns the data associated with an item at a specific index in the list box of a combo box button that has a specific command ID.  
  
## Syntax  
  
```  
static DWORD_PTR GetItemDataAll(  
   UINT uiCmd,  
   int iIndex=-1   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID of a combo box button.  
  
 [in] `iIndex`  
 The zero-based index of an item in the list box.  
  
## Return Value  
 The data associated with the item if the method was successful; otherwise, 0 if the specified index is not valid, or CB_ERR if the combo box button is not found.  
  
## Remarks  
 An index parameter of -1 returns the data associated with the currently selected item.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)