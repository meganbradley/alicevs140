---
title: "CDC::PolyDraw"
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
ms.assetid: 23c25cc4-ed47-4c39-b47a-e2c33641e76e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PolyDraw
Draws a set of line segments and Bzier splines.  
  
## Syntax  
  
```  
  
      BOOL PolyDraw(  
   const POINT* lpPoints,  
   const BYTE* lpTypes,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of [POINT](../vs140/POINT-Structure.md) data structures that contains the endpoints for each line segment and the endpoints and control points for each Bzier spline.  
  
 `lpTypes`  
 Points to an array that specifies how each point in the `lpPoints` array is used. Values can be one of the following:  
  
-   **PT_MOVETO** Specifies that this point starts a disjoint figure. This point becomes the new current position.  
  
-   **PT_LINETO** Specifies that a line is to be drawn from the current position to this point, which then becomes the new current position.  
  
-   **PT_BEZIERTO** Specifies that this point is a control point or ending point for a Bzier spline.  
  
     **PT_BEZIERTO** types always occur in sets of three. The current position defines the starting point for the Bzier spline. The first two **PT_BEZIERTO** points are the control points, and the third **PT_BEZIERTO** point is the ending point. The ending point becomes the new current position. If there are not three consecutive **PT_BEZIERTO** points, an error results.  
  
     A **PT_LINETO** or **PT_BEZIERTO** type can be combined with the following constant by using the bitwise operator OR to indicate that the corresponding point is the last point in a figure and the figure is closed:  
  
-   **PT_CLOSEFIGURE** Specifies that the figure is automatically closed after the **PT_LINETO** or **PT_BEZIERTO** type for this point is done. A line is drawn from this point to the most recent **PT_MOVETO** or `MoveTo` point.  
  
     This flag is combined with the **PT_LINETO** type for a line, or with the **PT_BEZIERTO** type of ending point for a Bzier spline, by using the bitwise `OR` operator. The current position is set to the ending point of the closing line.  
  
 `nCount`  
 Specifies the total number of points in the `lpPoints` array, the same as the number of bytes in the `lpTypes` array.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 This function can be used to draw disjoint figures in place of consecutive calls to `CDC::MoveTo`, `CDC::LineTo`, and `CDC::PolyBezierTo` member functions. The lines and splines are drawn using the current pen, and figures are not filled. If there is an active path started by calling the `CDC::BeginPath` member function, `PolyDraw` adds to the path. The points contained in the `lpPoints` array and in `lpTypes` indicate whether each point is part of a `CDC::MoveTo`, a `CDC::LineTo`, or a **CDC::BezierTo** operation. It is also possible to close figures. This function updates the current position.  
  
## Example  
 See the example for [CDC::BeginPath](../vs140/CDC--BeginPath.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::BeginPath](../vs140/CDC--BeginPath.md)   
 [CDC::EndPath](../vs140/CDC--EndPath.md)   
 [CDC::LineTo](../vs140/CDC--LineTo.md)   
 [CDC::MoveTo](../vs140/CDC--MoveTo.md)   
 [CDC::PolyBezierTo](../vs140/CDC--PolyBezierTo.md)   
 [CDC::Polyline](../vs140/CDC--Polyline.md)   
 [PolyDraw](http://msdn.microsoft.com/library/windows/desktop/dd162813)