---
title: "CRectTracker::TrackRubberBand"
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
ms.assetid: d2250bf3-c9f0-4059-990a-a83eeb65b079
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::TrackRubberBand
Call this function to do rubber-band selection.  
  
## Syntax  
  
```  
  
      BOOL TrackRubberBand(  
   CWnd* pWnd,  
   CPoint point,  
   BOOL bAllowInvert = TRUE   
);  
```  
  
#### Parameters  
 `pWnd`  
 The window object that contains the rectangle.  
  
 `point`  
 Device coordinates of the current mouse position relative to the client area.  
  
 `bAllowInvert`  
 If **TRUE,** the rectangle can be inverted along the x-axis or y-axis; otherwise **FALSE**.  
  
## Return Value  
 Nonzero if the mouse has moved and the rectangle is not empty; otherwise 0.  
  
## Remarks  
 It is usually called from inside the function of your application that handles the `WM_LBUTTONDOWN` message (typically `OnLButtonDown`).  
  
 This function will capture the mouse until the user releases the left mouse button, presses the ESC key, or presses the right mouse button. As the user moves the mouse cursor, the feedback is updated by calling `DrawTrackerRect` and `OnChangedRect`.  
  
 Tracking is performed with a rubber-band-type selection from the lower-right handle. If inverting is allowed, the rectangle can be sized by dragging either up and to the left or down and to the right.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRectTracker::DrawTrackerRect](../vs140/CRectTracker--DrawTrackerRect.md)   
 [CRectTracker::OnChangedRect](../vs140/CRectTracker--OnChangedRect.md)   
 [CRectTracker::CRectTracker](../vs140/CRectTracker--CRectTracker.md)