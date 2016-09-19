---
title: "CFrameWnd::DockControlBar"
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
ms.assetid: b34a2a37-64fe-49ff-a556-537bed35b970
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::DockControlBar
Causes a control bar to be docked to the frame window.  
  
## Syntax  
  
```  
  
      void DockControlBar(  
   CControlBar* pBar,  
   UINT nDockBarID = 0,  
   LPCRECT lpRect = NULL   
);  
```  
  
#### Parameters  
 `pBar`  
 Points to the control bar to be docked.  
  
 `nDockBarID`  
 Determines which sides of the frame window to consider for docking. It can be 0, or one or more of the following:  
  
-   `AFX_IDW_DOCKBAR_TOP` Dock to the top side of the frame window.  
  
-   **AFX_IDW_DOCKBAR_BOTTOM** Dock to the bottom side of the frame window.  
  
-   `AFX_IDW_DOCKBAR_LEFT` Dock to the left side of the frame window.  
  
-   `AFX_IDW_DOCKBAR_RIGHT` Dock to the right side of the frame window.  
  
 If 0, the control bar can be docked to any side enabled for docking in the destination frame window.  
  
 `lpRect`  
 Determines, in screen coordinates, where the control bar will be docked in the nonclient area of the destination frame window.  
  
## Remarks  
 The control bar will be docked to one of the sides of the frame window specified in the calls to both [CControlBar::EnableDocking](../vs140/CControlBar--EnableDocking.md) and [CFrameWnd::EnableDocking](../vs140/CFrameWnd--EnableDocking.md). The side chosen is determined by `nDockBarID`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::FloatControlBar](../vs140/CFrameWnd--FloatControlBar.md)