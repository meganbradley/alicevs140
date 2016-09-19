---
title: "CMFCRibbonComboBox::OnSelectItem"
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
ms.assetid: 860767ed-6e78-45ae-9fe3-9b27f4f0345b
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonComboBox::OnSelectItem
Called by the framework when a user selects an item in the list box.  
  
## Syntax  
  
```  
virtual void OnSelectItem(  
   int nItem   
);  
```  
  
#### Parameters  
 [in] `nItem`  
 The index of the selected item.  
  
## Remarks  
 Override this method if you want to process a user input selection.  
  
## Requirements  
 **Header:** afxribboncombobox.h  
  
## See Also  
 [CMFCRibbonComboBox Class](../vs140/CMFCRibbonComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)