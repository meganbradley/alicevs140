---
title: "CRectTracker::DrawTrackerRect"
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
ms.assetid: e5bf03f9-ce5d-4910-858e-5dbdbdc46bd7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::DrawTrackerRect
Called by the framework whenever the position of the tracker has changed while inside the `Track` or `TrackRubberBand` member function.  
  
## Syntax  
  
```  
  
      virtual void DrawTrackerRect(  
   LPCRECT lpRect,  
   CWnd* pWndClipTo,  
   CDC* pDC,  
   CWnd* pWnd   
);  
```  
  
#### Parameters  
 `lpRect`  
 Pointer to the `RECT` that contains the rectangle to draw.  
  
 `pWndClipTo`  
 Pointer to the window to use in clipping the rectangle.  
  
 `pDC`  
 Pointer to the device context on which to draw.  
  
 `pWnd`  
 Pointer to the window on which the drawing will occur.  
  
## Remarks  
 The default implementation makes a call to `CDC::DrawFocusRect`, which draws a dotted rectangle.  
  
 Override this function to provide different feedback during the tracking operation.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRectTracker::Track](../vs140/CRectTracker--Track.md)   
 [CRectTracker::TrackRubberBand](../vs140/CRectTracker--TrackRubberBand.md)   
 [CDC::DrawFocusRect](../vs140/CDC--DrawFocusRect.md)