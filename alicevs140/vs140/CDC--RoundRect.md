---
title: "CDC::RoundRect"
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
ms.assetid: c20e1713-7569-40a4-ac52-4c68cbc56f7c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::RoundRect
Draws a rectangle with rounded corners using the current pen.  
  
## Syntax  
  
```  
  
      BOOL RoundRect(  
   int x1,  
   int y1,  
   int x2,  
   int y2,  
   int x3,  
   int y3   
);  
BOOL RoundRect(  
   LPCRECT lpRect,  
   POINT point   
);  
```  
  
#### Parameters  
 `x1`  
 Specifies the x-coordinate of the upper-left corner of the rectangle (in logical units).  
  
 `y1`  
 Specifies the y-coordinate of the upper-left corner of the rectangle (in logical units).  
  
 `x2`  
 Specifies the x-coordinate of the lower-right corner of the rectangle (in logical units).  
  
 `y2`  
 Specifies the y-coordinate of the lower-right corner of the rectangle (in logical units).  
  
 *x3*  
 Specifies the width of the ellipse used to draw the rounded corners (in logical units).  
  
 `y3`  
 Specifies the height of the ellipse used to draw the rounded corners (in logical units).  
  
 `lpRect`  
 Specifies the bounding rectangle in logical units. You can pass either a `CRect` object or a pointer to a `RECT` structure for this parameter.  
  
 `point`  
 The x-coordinate of `point` specifies the width of the ellipse to draw the rounded corners (in logical units). The y-coordinate of `point` specifies the height of the ellipse to draw the rounded corners (in logical units). You can pass either a **POINT** structure or a `CPoint` object for this parameter.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The interior of the rectangle is filled using the current brush.  
  
 The figure this function draws extends up to but does not include the right and bottom coordinates. This means that the height of the figure is `y2` – `y1` and the width of the figure is `x2` – `x1`. Both the height and the width of the bounding rectangle must be greater than 2 units and less than 32,767 units.  
  
## Example  
 [!CODE [NVC_MFCDocView#40](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#40)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Rectangle](../vs140/CDC--Rectangle.md)   
 [RoundRect](http://msdn.microsoft.com/library/windows/desktop/dd162944)   
 [CRect Class](../vs140/CRect-Class.md)   
 [RECT Structure](../vs140/RECT-Structure.md)   
 [POINT Structure](../vs140/POINT-Structure.md)   
 [CPoint Class](../vs140/CPoint-Class.md)