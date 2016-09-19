---
title: "CMFCRibbonBar::SetMaximizeMode"
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
ms.assetid: 8b6bea72-b771-43e7-955c-a034a457d081
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::SetMaximizeMode
Adjusts the ribbon bar when the window size of a multiple-document interface (MDI) child window enters or leaves the maximized state.  
  
## Syntax  
  
```  
void SetMaximizeMode(  
   BOOL bMax,  
   CWnd* pWnd = NULL  
);  
```  
  
#### Parameters  
 [in] `bMax`  
 `TRUE` to display the system buttons for an MDI child window on the ribbon bar; `FALSE` to remove the system buttons for an MDI child window from the ribbon bar.  
  
 [in] `pWnd`  
 Pointer to the main frame window for the ribbon bar.  
  
## Remarks  
 The ribbon bar displays system buttons for an MDI child window in the tab row when an MDI child window is maximized.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)