---
title: "CMFCPropertyGridCtrl::SetShowDragContext"
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
ms.assetid: a719847f-76f3-43d0-b84c-b8b0b144e018
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::SetShowDragContext
Specifies whether the framework redraws the name and value columns of the current property grid control when a user resizes the columns.  
  
## Syntax  
  
```  
void SetShowDragContext(  
   BOOL bShowDragContext = TRUE  
);  
```  
  
#### Parameters  
 [in] `bShowDragContext`  
 `TRUE` to redraw the name and value columns during a resize operation; `FALSE` to redraw the columns after the drag operation is completed. The default value is `TRUE`.  
  
## Remarks  
 The user can resize the name and value columns of a property grid control by dragging the split bar that is between the columns. If the drag context is displayed, the name and value columns are resized as long as the user drags the split bar. Otherwise, the split bar moves but the columns are not redrawn until the drag operation is completed.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridCtrl::IsShowDragContext](../vs140/CMFCPropertyGridCtrl--IsShowDragContext.md)