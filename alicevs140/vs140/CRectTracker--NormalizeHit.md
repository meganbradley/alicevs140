---
title: "CRectTracker::NormalizeHit"
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
ms.assetid: d4bf920a-4189-48ab-9f52-972525e64b1b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::NormalizeHit
Call this function to convert a potentially inverted handle.  
  
## Syntax  
  
```  
  
      int NormalizeHit(  
   int nHandle   
) const;  
```  
  
#### Parameters  
 `nHandle`  
 Handle selected by the user.  
  
## Return Value  
 The index of the normalized handle.  
  
## Remarks  
 When `CRectTracker::Track` or `CRectTracker::TrackRubberBand` is called with inverting allowed, it is possible for the rectangle to be inverted on the x-axis, the y-axis, or both. When this happens, `HitTest` will return handles that are also inverted with respect to the rectangle. This is inappropriate for drawing cursor feedback because the feedback depends on the screen position of the rectangle, not the portion of the rectangle data structure that will be modified.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRectTracker::HitTest](../vs140/CRectTracker--HitTest.md)   
 [CRectTracker::Track](../vs140/CRectTracker--Track.md)   
 [CRectTracker::TrackRubberBand](../vs140/CRectTracker--TrackRubberBand.md)