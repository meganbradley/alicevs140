---
title: "CDC::MoveTo"
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
ms.assetid: 3fe1531e-2d59-4c11-b25f-4cea279e73d0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::MoveTo
Moves the current position to the point specified by *x* and *y* (or by `point`).  
  
## Syntax  
  
```  
  
      CPoint MoveTo(  
   int x,  
   int y   
);  
CPoint MoveTo(  
   POINT point   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the new position.  
  
 *y*  
 Specifies the logical y-coordinate of the new position.  
  
 `point`  
 Specifies the new position. You can pass either a **POINT** structure or a `CPoint` object for this parameter.  
  
## Return Value  
 The x- and y-coordinates of the previous position as a `CPoint` object.  
  
## Example  
 See the example for [CRect::CenterPoint](../vs140/CRect--CenterPoint.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetCurrentPosition](../vs140/CDC--GetCurrentPosition.md)   
 [CDC::LineTo](../vs140/CDC--LineTo.md)   
 [CPoint Class](../vs140/CPoint-Class.md)   
 [POINT Structure](../vs140/POINT-Structure.md)