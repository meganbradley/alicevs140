---
title: "CDC::Polygon"
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
ms.assetid: a2621785-7f54-49fd-8ef1-3fa558e9b6fd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::Polygon
Draws a polygon consisting of two or more points (vertices) connected by lines, using the current pen.  
  
## Syntax  
  
```  
  
      BOOL Polygon(  
   LPPOINT lpPoints,  
   int nCount   
);  
```  
  
#### Parameters  
 `lpPoints`  
 Points to an array of points that specifies the vertices of the polygon. Each point in the array is a **POINT** structure or a `CPoint` object.  
  
 `nCount`  
 Specifies the number of vertices in the array.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 The system closes the polygon automatically, if necessary, by drawing a line from the last vertex to the first.  
  
 The current polygon-filling mode can be retrieved or set by using the `GetPolyFillMode` and `SetPolyFillMode` member functions.  
  
## Example  
 [!CODE [NVC_MFCDocView#38](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#38)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::GetPolyFillMode](../vs140/CDC--GetPolyFillMode.md)   
 [CDC::Polyline](../vs140/CDC--Polyline.md)   
 [CDC::PolyPolygon](../vs140/CDC--PolyPolygon.md)   
 [CDC::SetPolyFillMode](../vs140/CDC--SetPolyFillMode.md)   
 [CPoint Class](../vs140/CPoint-Class.md)   
 [Polygon](http://msdn.microsoft.com/library/windows/desktop/dd162814)