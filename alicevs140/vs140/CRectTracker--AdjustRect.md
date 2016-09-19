---
title: "CRectTracker::AdjustRect"
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
ms.assetid: 730bf555-0f8e-4b8f-a310-0d9c72697e8f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::AdjustRect
Called by the framework when the tracking rectangle is resized by using a resize handle.  
  
## Syntax  
  
```  
  
      virtual void AdjustRect(  
   int nHandle,  
   LPRECT lpRect   
);  
```  
  
#### Parameters  
 `nHandle`  
 Index of handle used.  
  
 `lpRect`  
 Pointer to the current size of the rectangle. (The size of a rectangle is given by its height and width.)  
  
## Remarks  
 The default behavior of this function allows the rectangle's orientation to change only when `Track` and `TrackRubberBand` are called with inverting allowed.  
  
 Override this function to control the adjustment of the tracking rectangle during a dragging operation. One method is to adjust the coordinates specified by `lpRect` before returning.  
  
 Special features that are not directly supported by `CRectTracker`, such as snap-to-grid or keep-aspect-ratio, can be implemented by overriding this function.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRectTracker::Track](../vs140/CRectTracker--Track.md)   
 [CRectTracker::TrackRubberBand](../vs140/CRectTracker--TrackRubberBand.md)   
 [CRectTracker::OnChangedRect](../vs140/CRectTracker--OnChangedRect.md)