---
title: "CMFCMenuBar::SetMaximizeMode"
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
ms.assetid: 92fcad99-2d44-40a8-9691-65779e6b903c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::SetMaximizeMode
The framework calls this method when a MDI changes its display mode and the menu bar must be updated.  
  
## Syntax  
  
```  
void SetMaximizeMode(  
   BOOL bMax,  
   CWnd* pWnd = NULL,  
   BOOL bRecalcLayout = TRUE  
);  
```  
  
#### Parameters  
 [in] `bMax`  
 A Boolean that specifies the mode. See the Remarks section for more information.  
  
 [in] `pWnd`  
 A pointer to the MDI child window that is changing.  
  
 [in] `bRecalcLayout`  
 A Boolean that specifies whether the layout of the menu bar should be recalculated immediately.  
  
## Remarks  
 When an MDI child window is maximized, a menu bar attached to the MDI main frame window displays the system menu and the **Minimize**, **Maximize** and **Close** buttons. If `bMax` is `TRUE` and `pWnd` is not `NULL`, the MDI child window is maximized and the menu bar must incorporate the extra controls. Otherwise, the menu bar returns to its regular state.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)