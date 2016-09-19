---
title: "CDC::Rectangle"
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
ms.assetid: 63a3f745-7815-4747-b96d-7c6e7374a274
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::Rectangle
Draws a rectangle using the current pen.  
  
## Syntax  
  
```  
  
      BOOL Rectangle(  
   int x1,  
   int y1,  
   int x2,  
   int y2   
);  
BOOL Rectangle(  
   LPCRECT lpRect   
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
  
 `lpRect`  
 Specifies the rectangle in logical units. You can pass either a `CRect` object or a pointer to a `RECT` structure for this parameter.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The interior of the rectangle is filled using the current brush.  
  
 The rectangle extends up to, but does not include, the right and bottom coordinates. This means that the height of the rectangle is `y2` – `y1` and the width of the rectangle is `x2` – `x1`. Both the width and the height of a rectangle must be greater than 2 units and less than 32,767 units.  
  
## Example  
 [!CODE [NVC_MFCDocView#39](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#39)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Rectangle](http://msdn.microsoft.com/library/windows/desktop/dd162898)   
 [CDC::Polyline](../vs140/CDC--Polyline.md)   
 [CDC::RoundRect](../vs140/CDC--RoundRect.md)   
 [RECT Structure](../vs140/RECT-Structure.md)   
 [CRect Class](../vs140/CRect-Class.md)