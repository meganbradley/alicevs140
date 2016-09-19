---
title: "CMFCPropertyGridCtrl::IsShowDragContext"
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
ms.assetid: 6926f2b4-af3d-445a-abff-dc3fa9d01800
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertyGridCtrl::IsShowDragContext
Indicates whether the framework redraws the name and value columns of the current property grid control when a user resizes the columns.  
  
## Syntax  
  
```  
BOOL IsShowDragContext() const;  
```  
  
## Return Value  
 `TRUE` if the framework redraws the name and value columns during a resize operation; `FALSE` if the framework redraws the columns after the drag operation is completed.  
  
## Remarks  
 The user can resize the name and value columns of a property grid control by dragging the split bar that is between the columns. If the drag context is displayed, the name and value columns are resized as long as the user drags the split bar. Otherwise, the split bar moves but the columns are not redrawn until the drag operation is completed.  
  
## Requirements  
 **Header:** afxpropertygridctrl.h  
  
## See Also  
 [CMFCPropertyGridCtrl Class](../vs140/CMFCPropertyGridCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCPropertyGridCtrl::SetShowDragContext](../vs140/CMFCPropertyGridCtrl--SetShowDragContext.md)