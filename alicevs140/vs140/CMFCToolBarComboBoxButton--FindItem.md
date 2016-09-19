---
title: "CMFCToolBarComboBoxButton::FindItem"
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
ms.assetid: 00229ee9-f095-48ac-8be9-6629c8ce7053
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::FindItem
Returns the index of the first item in the list box that contains a specified string.  
  
## Syntax  
  
```  
int FindItem(  
   LPCTSTR lpszText   
) const;  
```  
  
#### Parameters  
 [in] `lpszText`  
 The text for which to search in the list box.  
  
## Return Value  
 The index of the item; or `CB_ERR` if the item is not found.  
  
## Remarks  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)