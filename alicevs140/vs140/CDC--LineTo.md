---
title: "CDC::LineTo"
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
ms.assetid: 2a4b0c65-8189-4bca-aa6b-35d29995cfc2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::LineTo
Draws a line from the current position up to, but not including, the point specified by *x* and *y* (or `point`).  
  
## Syntax  
  
```  
  
      BOOL LineTo(  
   int x,  
   int y   
);  
BOOL LineTo(  
   POINT point   
);  
```  
  
#### Parameters  
 *x*  
 Specifies the logical x-coordinate of the endpoint for the line.  
  
 *y*  
 Specifies the logical y-coordinate of the endpoint for the line.  
  
 `point`  
 Specifies the endpoint for the line. You can pass either a **POINT** structure or a `CPoint` object for this parameter.  
  
## Return Value  
 Nonzero if the line is drawn; otherwise 0.  
  
## Remarks  
 The line is drawn with the selected pen. The current position is set to *x*,*y* or to `point`.  
  
## Example  
 See the example for [CRect::CenterPoint](../vs140/CRect--CenterPoint.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::MoveTo](../vs140/CDC--MoveTo.md)   
 [CDC::GetCurrentPosition](../vs140/CDC--GetCurrentPosition.md)   
 [LineTo](http://msdn.microsoft.com/library/windows/desktop/dd145029)   
 [CPoint Class](../vs140/CPoint-Class.md)   
 [POINT Structure](../vs140/POINT-Structure.md)