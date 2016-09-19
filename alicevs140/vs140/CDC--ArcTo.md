---
title: "CDC::ArcTo"
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
ms.assetid: fa9021f9-30c0-4cb0-bcb6-6c40131a263f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::ArcTo
Draws an elliptical arc.  
  
## Syntax  
  
```  
  
      BOOL ArcTo(  
   int x1,  
   int y1,  
   int x2,  
   int y2,  
   int x3,  
   int y3,  
   int x4,  
   int y4   
);  
BOOL ArcTo(  
   LPCRECT lpRect,  
   POINT ptStart,  
   POINT ptEnd   
);  
```  
  
#### Parameters  
 `x1`  
 Specifies the x-coordinate of the upper-left corner of the bounding rectangle (in logical units).  
  
 `y1`  
 Specifies the y-coordinate of the upper-left corner of the bounding rectangle (in logical units).  
  
 `x2`  
 Specifies the x-coordinate of the lower-right corner of the bounding rectangle (in logical units).  
  
 `y2`  
 Specifies the y-coordinate of the lower-right corner of the bounding rectangle (in logical units).  
  
 *x3*  
 Specifies the x-coordinate of the point that defines the arc's starting point (in logical units). This point does not have to lie exactly on the arc.  
  
 `y3`  
 Specifies the y-coordinate of the point that defines the arc's starting point (in logical units). This point does not have to lie exactly on the arc.  
  
 `x4`  
 Specifies the x-coordinate of the point that defines the arc's endpoint (in logical units). This point does not have to lie exactly on the arc.  
  
 `y4`  
 Specifies the y-coordinate of the point that defines the arc's endpoint (in logical units). This point does not have to lie exactly on the arc.  
  
 `lpRect`  
 Specifies the bounding rectangle (in logical units). You can pass either a pointer to a [RECT](../vs140/RECT-Structure.md) data structure or a [CRect](../vs140/CRect-Class.md) object for this parameter.  
  
 `ptStart`  
 Specifies the x- and y-coordinates of the point that defines the arc's starting point (in logical units). This point does not have to lie exactly on the arc. You can pass either a [POINT](../vs140/POINT-Structure.md) data structure or a [CPoint](../vs140/CPoint-Class.md) object for this parameter.  
  
 `ptEnd`  
 Specifies the x- and y-coordinates of the point that defines the arc's ending point (in logical units). This point does not have to lie exactly on the arc. You can pass either a **POINT** data structure or a `CPoint` object for this parameter.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 This function is similar to `CDC::Arc`, except that the current position is updated. The points (`x1`,`y1`) and (`x2`,`y2`) specify the bounding rectangle. An ellipse formed by the given bounding rectangle defines the curve of the arc. The arc extends counterclockwise (the default arc direction) from the point where it intersects the radial line from the center of the bounding rectangle to (*x3*,`y3`). The arc ends where it intersects the radial line from the center of the bounding rectangle to (`x4`,`y4`). If the starting point and ending point are the same, a complete ellipse is drawn.  
  
 A line is drawn from the current position to the starting point of the arc. If no error occurs, the current position is set to the ending point of the arc. The arc is drawn using the current pen; it is not filled.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::AngleArc](../vs140/CDC--AngleArc.md)   
 [CDC::Arc](../vs140/CDC--Arc.md)   
 [CDC::SetArcDirection](../vs140/CDC--SetArcDirection.md)   
 [ArcTo](http://msdn.microsoft.com/library/windows/desktop/dd183358)