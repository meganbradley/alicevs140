---
title: "CDC::Polyline"
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
ms.assetid: afb30642-057a-46ef-b7df-61a4397be3b0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::Polyline
Draws a set of line segments connecting the points specified by `lpPoints`.  
  
## Syntax  
  
```  
  
      BOOL Polyline(  
   LPPOINT lpPoints,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of **POINT** structures or `CPoint` objects to be connected.  
  
 `nCount`  
 Specifies the number of points in the array. This value must be at least 2.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The lines are drawn from the first point through subsequent points using the current pen. Unlike the `LineTo` member function, the `Polyline` function neither uses nor updates the current position.  
  
 For more information, see [PolyLine](http://msdn.microsoft.com/library/windows/desktop/dd162815) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::LineTo](../vs140/CDC--LineTo.md)   
 [CDC::Polygon](../vs140/CDC--Polygon.md)   
 [POINT Structure](../vs140/POINT-Structure.md)   
 [CPoint Class](../vs140/CPoint-Class.md)