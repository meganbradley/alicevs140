---
title: "CMDIFrameWndEx::RemovePaneFromDockManager"
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
ms.assetid: 81b35c8b-adf4-4a64-a4ec-1701bc11d64a
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::RemovePaneFromDockManager
Unregisters a pane and removes it from the docking manager.  
  
## Syntax  
  
```  
void RemovePaneFromDockManager(  
   CBasePane* pControlBar,  
   BOOL bDestroy,  
   BOOL bAdjustLayout,  
   BOOL bAutoHide,  
   CBasePane* pBarReplacement   
);  
```  
  
#### Parameters  
 [in] `pControlBar`  
 A pointer to a pane to be removed.  
  
 [in] `bDestroy`  
 `TRUE` to destroy the removed pane. `FALSE` to not destroy it.  
  
 [in] `bAdjustLayout`  
 `TRUE` to adjust the docking layout immediately. If `FALSE`, the adjustment will occur only when a redraw event occurs for other reasons (the user resizes the window, drags the main frame, etc.).  
  
 [in] `bAutoHide`  
 `TRUE` to remove the pane from the list of autohide panes. `FALSE` to remove the pane from the list of regular panes.  
  
 [in] `pBarReplacement`  
 A pointer to a pane that replaces the removed pane.  
  
## Remarks  
 You must register each pane with the docking manager to take part in the docking layout. Use [CMDIFrameWndEx::AddPane](../vs140/CMDIFrameWndEx--AddPane.md) or [CMDIFrameWndEx::InsertPane](../vs140/CMDIFrameWndEx--InsertPane.md) to register panes.  
  
 Use this method when a pane is no longer a part of the docking layout of the frame window.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockingManager Class](../vs140/CDockingManager-Class.md)