---
title: "CDC::PolyBezier"
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
ms.assetid: 2c57937a-348d-48d3-a027-961466df9366
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PolyBezier
Draws one or more Bzier splines.  
  
## Syntax  
  
```  
  
      BOOL PolyBezier(  
   const POINT* lpPoints,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of [POINT](../vs140/POINT-Structure.md) data structures that contain the endpoints and control points of the spline(s).  
  
 `nCount`  
 Specifies the number of points in the `lpPoints` array. This value must be one more than three times the number of splines to be drawn, because each Bzier spline requires two control points and an endpoint, and the initial spline requires an additional starting point.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 This function draws cubic Bzier splines by using the endpoints and control points specified by the `lpPoints` parameter. The first spline is drawn from the first point to the fourth point by using the second and third points as control points. Each subsequent spline in the sequence needs exactly three more points: the end point of the previous spline is used as the starting point, the next two points in the sequence are control points, and the third is the end point.  
  
 The current position is neither used nor updated by the `PolyBezier` function. The figure is not filled. This function draws lines by using the current pen.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::PolyBezierTo](../vs140/CDC--PolyBezierTo.md)   
 [PolyBezier](http://msdn.microsoft.com/library/windows/desktop/dd162811)