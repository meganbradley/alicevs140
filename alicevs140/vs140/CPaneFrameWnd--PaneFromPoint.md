---
title: "CPaneFrameWnd::PaneFromPoint"
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
ms.assetid: 68780d0b-3229-40e7-9613-d39b4cfc16ed
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::PaneFromPoint
Returns a pane if it contains a user-supplied point inside a mini-frame window.  
  
## Syntax  
  
```  
virtual CBasePane* PaneFromPoint(  
    CPoint point,  
    int nSensitivity,  
    BOOL bCheckVisibility  
);  
```  
  
#### Parameters  
 [in] `point`  
 The point that the user clicked, in screen coordinates.  
  
 [in] `nSensitivity`  
 This parameter is not used.  
  
 [in] `bCheckVisibility`  
 `TRUE` to specify that only visible panes should be returned; otherwise, `FALSE`.  
  
## Return Value  
 The pane that the user clicked, or `NULL` if no pane exists at that location.  
  
## Remarks  
 Call this method to obtain a pane that contains the given point.  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)