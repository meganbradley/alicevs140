---
title: "CDC::PolyPolygon"
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
ms.assetid: 168d7220-637a-4ccf-8fb1-0b9f09a01fef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::PolyPolygon
Creates two or more polygons that are filled using the current polygon-filling mode.  
  
## Syntax  
  
```  
  
      BOOL PolyPolygon(  
   LPPOINT lpPoints,  
   LPINT lpPolyCounts,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of **POINT** structures or `CPoint` objects that define the vertices of the polygons.  
  
 `lpPolyCounts`  
 Points to an array of integers, each of which specifies the number of points in one of the polygons in the `lpPoints` array.  
  
 `nCount`  
 The number of entries in the `lpPolyCounts` array. This number specifies the number of polygons to be drawn. This value must be at least 2.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The polygons may be disjoint or overlapping.  
  
 Each polygon specified in a call to the `PolyPolygon` function must be closed. Unlike polygons created by the **Polygon** member function, the polygons created by `PolyPolygon` are not closed automatically.  
  
 The function creates two or more polygons. To create a single polygon, an application should use the **Polygon** member function.  
  
 The current polygon-filling mode can be retrieved or set by using the `GetPolyFillMode` and `SetPolyFillMode` member functions.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetPolyFillMode](../vs140/CDC--GetPolyFillMode.md)   
 [CDC::Polygon](../vs140/CDC--Polygon.md)   
 [CDC::Polyline](../vs140/CDC--Polyline.md)   
 [CDC::SetPolyFillMode](../vs140/CDC--SetPolyFillMode.md)   
 [PolyPolygon](http://msdn.microsoft.com/library/windows/desktop/dd162818)   
 [POINT Structure](../vs140/POINT-Structure.md)   
 [CPoint Class](../vs140/CPoint-Class.md)