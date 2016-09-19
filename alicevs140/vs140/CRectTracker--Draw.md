---
title: "CRectTracker::Draw"
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
ms.assetid: 00740987-a321-4484-a7c0-403380cb6188
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::Draw
Call this function to draw the rectangle's outer lines and inner region.  
  
## Syntax  
  
```  
  
      void Draw(  
   CDC* pDC   
) const;  
```  
  
#### Parameters  
 `pDC`  
 Pointer to the device context on which to draw.  
  
## Remarks  
 The style of the tracker determines how the drawing is done. See the constructor for `CRectTracker` for more information on the styles available.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRectTracker::DrawTrackerRect](../vs140/CRectTracker--DrawTrackerRect.md)   
 [CRectTracker::CRectTracker](../vs140/CRectTracker--CRectTracker.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)