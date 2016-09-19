---
title: "CMFCToolBar::StretchPane"
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
ms.assetid: 9b0b359e-839b-47ca-b172-1ed37b952dfd
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::StretchPane
Stretches the toolbar vertically or horizontally, and repositions the buttons if necessary.  
  
## Syntax  
  
```  
virtual CSize StretchPane(  
   int nLength,  
   BOOL bVert  
);  
```  
  
#### Parameters  
 [in] `nLength`  
 The amount, in pixels, by which to stretch the pane.  
  
 [in] `bVert`  
 If `TRUE`, stretches the pane vertically. If `FALSE`, stretches the pane horizontally.  
  
## Return Value  
 A `CSize` object that specifies the size of the toolbar client area.  
  
## Remarks  
 This method calls [CMFCToolBar::WrapToolBar](../vs140/CMFCToolBar--WrapToolBar.md) to reposition the buttons within the stretched toolbar.  
  
 The return value is determined by calling [CMFCToolBar::CalcSize](../vs140/CMFCToolBar--CalcSize.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)