---
title: "CFrameWndEx::RemovePaneFromDockManager"
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
ms.assetid: 3462a0eb-78ac-4805-9b11-d3176f4b1194
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::RemovePaneFromDockManager
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
 A pointer to the control bar pane to remove.  
  
 [in] `bDestroy`  
 `TRUE` to destroy the control bar after removing it; `FALSE` otherwise.  
  
 [in] `bAdjustLayout`  
 `TRUE` to adjust the docking layout; `FALSE` otherwise.  
  
 [in] `bAutoHide`  
 `TRUE` if the control bar is in auto-hide mode; `FALSE` otherwise.  
  
 [in] `pBarReplacement`  
 A pointer to a pane that replaces the removed pane.  
  
## Remarks  
 Use this method to remove a control bar from the docking layout of the frame window.  
  
 The [CDockingManager Class](../vs140/CDockingManager-Class.md) handles the layout of control bars. You must register each control bar with the docking manager by using the [CFrameWndEx::AddPane](../vs140/CFrameWndEx--AddPane.md) method or the [CFrameWndEx::InsertPane](../vs140/CFrameWndEx--InsertPane.md) method.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)