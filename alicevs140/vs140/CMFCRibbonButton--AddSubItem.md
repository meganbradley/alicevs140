---
title: "CMFCRibbonButton::AddSubItem"
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
ms.assetid: 5e5d3129-a892-48ba-8a62-eda1f5769e39
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButton::AddSubItem
Adds a menu item to the pop-up menu that is associated with the button.  
  
## Syntax  
  
```  
void AddSubItem(  
   CMFCRibbonBaseElement* pSubItem,  
   int nIndex=-1   
);  
```  
  
#### Parameters  
 [in] `pSubItem`  
 Specifies a pointer to the new element to add.  
  
 [in] `nIndex`  
 Specifies the index at which to add the element to the array of menu items of the button; -1 to add the element at the end of the array of menu items.  
  
## Requirements  
 **Header:** afxribbonbutton.h  
  
## See Also  
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)