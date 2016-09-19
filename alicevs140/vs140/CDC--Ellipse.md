---
title: "CDC::Ellipse"
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
ms.assetid: a77eaab4-a1b7-4108-a611-a242a97c4377
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::Ellipse
Draws an ellipse.  
  
## Syntax  
  
```  
  
      BOOL Ellipse(  
   int x1,  
   int y1,  
   int x2,  
   int y2   
);  
BOOL Ellipse(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `x1`  
 Specifies the logical x-coordinate of the upper-left corner of the ellipse's bounding rectangle.  
  
 `y1`  
 Specifies the logical y-coordinate of the upper-left corner of the ellipse's bounding rectangle.  
  
 `x2`  
 Specifies the logical x-coordinate of the lower-right corner of the ellipse's bounding rectangle.  
  
 `y2`  
 Specifies the logical y-coordinate of the lower-right corner of the ellipse's bounding rectangle.  
  
 `lpRect`  
 Specifies the ellipse's bounding rectangle. You can also pass a [CRect](../vs140/CRect-Class.md) object for this parameter.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The center of the ellipse is the center of the bounding rectangle specified by `x1`, `y1`, `x2`, and `y2`, or `lpRect`. The ellipse is drawn with the current pen, and its interior is filled with the current brush.  
  
 The figure drawn by this function extends up to, but does not include, the right and bottom coordinates. This means that the height of the figure is `y2` – `y1` and the width of the figure is `x2` – `x1`.  
  
 If either the width or the height of the bounding rectangle is 0, no ellipse is drawn.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::Arc](../vs140/CDC--Arc.md)   
 [CDC::Chord](../vs140/CDC--Chord.md)   
 [Ellipse](http://msdn.microsoft.com/library/windows/desktop/dd162510)