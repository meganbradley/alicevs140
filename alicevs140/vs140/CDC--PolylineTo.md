---
title: "CDC::PolylineTo"
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
ms.assetid: 94e4a0db-78f0-4e28-9621-94d9647038f3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PolylineTo
Draws one or more straight lines.  
  
## Syntax  
  
```  
  
      BOOL PolylineTo(  
   const POINT* lpPoints,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of [POINT](../vs140/POINT-Structure.md) data structures that contains the vertices of the line.  
  
 `nCount`  
 Specifies the number of points in the array.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 A line is drawn from the current position to the first point specified by the `lpPoints` parameter by using the current pen. For each additional line, the function draws from the ending point of the previous line to the next point specified by `lpPoints`. `PolylineTo` moves the current position to the ending point of the last line. If the line segments drawn by this function form a closed figure, the figure is not filled.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::LineTo](../vs140/CDC--LineTo.md)   
 [CDC::Polyline](../vs140/CDC--Polyline.md)   
 [CDC::MoveTo](../vs140/CDC--MoveTo.md)   
 [PolylineTo](http://msdn.microsoft.com/library/windows/desktop/dd162816)