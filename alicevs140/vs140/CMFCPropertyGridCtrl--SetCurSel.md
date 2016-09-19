---
title: "CMFCPropertyGridCtrl::SetCurSel"
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
ms.assetid: b2631918-af89-46d0-94e3-1ea026e999a2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::SetCurSel
Selects a property in a property grid control.  
  
## Syntax  
  
```  
void SetCurSel(  
   CMFCPropertyGridProperty* pProp,  
   BOOL bRedraw=TRUE   
);  
```  
  
#### Parameters  
 [in] `pProp`  
 A pointer to a property object.  
  
 [in] `bRedraw`  
 `TRUE` to redraw the property grid control immediately; otherwise, `FALSE`. The default value is `TRUE`.  
  
## Remarks  
 Use this method to cancel the selection of the current item in the property grid control and then select the item that corresponds to the specified property.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)