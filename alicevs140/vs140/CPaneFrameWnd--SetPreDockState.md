---
title: "CPaneFrameWnd::SetPreDockState"
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
ms.assetid: 4c9c81ab-ca46-4984-bad0-416b95c7575c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::SetPreDockState
Called by the framework to set the predocking state.  
  
## Syntax  
  
```  
virtual BOOL SetPreDockState(  
   AFX_PREDOCK_STATE preDockState,  
   CBasePane* pBarToDock = NULL,  
   AFX_DOCK_METHOD dockMethod = DM_MOUSE  
);  
```  
  
#### Parameters  
 [in] `preDockState`  
 Possible values:  
  
-   `PDS_NOTHING`,  
  
-   `PDS_DOCK_REGULAR`,  
  
-   `PDS_DOCK_TO_TAB`  
  
 [in] `pBarToDock`  
 A pointer to the pane to dock.  
  
 [in] `dockMethod`  
 The docking method. (This parameter is ignored.)  
  
## Return Value  
 `TRUE` if the mini-frame window is undocked; `FALSE` if it is docked.  
  
## Requirements  
 **Header:** afxpaneframewnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)