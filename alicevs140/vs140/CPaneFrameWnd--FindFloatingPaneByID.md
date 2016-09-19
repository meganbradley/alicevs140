---
title: "CPaneFrameWnd::FindFloatingPaneByID"
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
ms.assetid: 4350c34d-3b5a-40b2-9f17-1d103a8fe7ed
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::FindFloatingPaneByID
Finds a pane with the specified control ID in the global list of floating panes.  
  
## Syntax  
  
```  
static CBasePane* FindFloatingPaneByID(  
    UINT nID  
);  
```  
  
#### Parameters  
 [in] `nID`  
 Represents the control ID of the pane to find.  
  
## Return Value  
 The pane with the specified control ID; otherwise, `NULL`, if no pane has the specified control ID.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)