---
title: "CMFCStatusBar::SetPaneBackgroundColor"
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
ms.assetid: 1b4bf4d3-4261-446f-a3da-c7847826e11f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCStatusBar::SetPaneBackgroundColor
Sets the background color of the status bar pane.  
  
## Syntax  
  
```  
void SetPaneBackgroundColor(  
   int nIndex,  
   COLORREF clrBackground=(COLORREF)-1,  
   BOOL bUpdate=TRUE   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of the pane for which to set a new background color.  
  
 [in] `clrBackground`  
 Specifies the new background color.  
  
 [in] `bUpdate`  
 If `TRUE`, update the pane content immediately. Otherwise, do not update the pane content until the pane is invalidated by another method.  
  
## Requirements  
 **Header:** afxstatusbar.h  
  
## See Also  
 [CMFCStatusBar Class](../vs140/CMFCStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)