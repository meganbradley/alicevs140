---
title: "CDC::PolyBezierTo"
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
ms.assetid: c7783261-ff4e-4fa8-9d78-0c91071c4898
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PolyBezierTo
Draws one or more Bzier splines.  
  
## Syntax  
  
```  
  
      BOOL PolyBezierTo(  
   const POINT* lpPoints,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of [POINT](../vs140/POINT-Structure.md) data structures that contains the endpoints and control points.  
  
 `nCount`  
 Specifies the number of points in the `lpPoints` array. This value must be three times the number of splines to be drawn, because each Bzier spline requires two control points and an end point.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 This function draws cubic Bzier splines by using the control points specified by the `lpPoints` parameter. The first spline is drawn from the current position to the third point by using the first two points as control points. For each subsequent spline, the function needs exactly three more points, and uses the end point of the previous spline as the starting point for the next. `PolyBezierTo` moves the current position to the end point of the last Bzier spline. The figure is not filled. This function draws lines by using the current pen.  
  
## Example  
 See the example for [CDC::BeginPath](../vs140/CDC--BeginPath.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::MoveTo](../vs140/CDC--MoveTo.md)   
 [CDC::PolyBezier](../vs140/CDC--PolyBezier.md)   
 [PolyBezierTo](http://msdn.microsoft.com/library/windows/desktop/dd162812)