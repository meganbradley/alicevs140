---
title: "CRectTracker::GetTrueRect"
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
ms.assetid: dad93d71-2014-483f-9dc8-a4220354d12f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::GetTrueRect
Call this function to retrieve the coordinates of the rectangle.  
  
## Syntax  
  
```  
  
      void GetTrueRect(  
   LPRECT lpTrueRect   
) const;  
```  
  
#### Parameters  
 `lpTrueRect`  
 Pointer to the `RECT` structure that will contain the device coordinates of the `CRectTracker` object.  
  
## Remarks  
 The dimensions of the rectangle include the height and width of any resize handles located on the outer border. Upon returning, `lpTrueRect` is always a normalized rectangle in device coordinates.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::NormalizeRect](../vs140/CRect--NormalizeRect.md)