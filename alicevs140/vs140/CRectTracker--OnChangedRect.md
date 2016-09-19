---
title: "CRectTracker::OnChangedRect"
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
ms.assetid: 24013d2a-cb86-4033-aa6d-67601c7a456e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::OnChangedRect
Called by the framework whenever the tracker rectangle has changed during a call to `Track`.  
  
## Syntax  
  
```  
  
      virtual void OnChangedRect(  
   const CRect& rectOld   
);  
```  
  
#### Parameters  
 *rectOld*  
 Contains the old device coordinates of the `CRectTracker` object.  
  
## Remarks  
 At the time this function is called, all feedback drawn with `DrawTrackerRect` has been removed. The default implementation of this function does nothing.  
  
 Override this function when you want to perform any actions after the rectangle has been resized.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRectTracker::AdjustRect](../vs140/CRectTracker--AdjustRect.md)   
 [CRectTracker::Track](../vs140/CRectTracker--Track.md)   
 [CRectTracker::TrackRubberBand](../vs140/CRectTracker--TrackRubberBand.md)