---
title: "CMFCHeaderCtrl::OnDrawItem"
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
ms.assetid: f46d80f0-f5dd-4f2e-aa2a-42dc7f6771b7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCHeaderCtrl::OnDrawItem
Called by the framework to draw a header control column.  
  
## Syntax  
  
```  
virtual void OnDrawItem(  
   CDC* pDC,  
   int iItem,  
   CRect rect,  
   BOOL bIsPressed,  
   BOOL bIsHighlighted   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `iItem`  
 The zero-based index of the item to draw.  
  
 [in] `rect`  
 The bounding rectangle of the item to draw.  
  
 [in] `bIsPressed`  
 `TRUE` to draw the item in pressed state; otherwise, `FALSE`.  
  
 [in] `bIsHighlighted`  
 `TRUE` to draw the item in highlighted state; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxheaderctrl.h  
  
## See Also  
 [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)