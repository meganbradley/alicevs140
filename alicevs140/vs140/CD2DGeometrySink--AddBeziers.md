---
title: "CD2DGeometrySink::AddBeziers"
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
ms.assetid: f52f0318-5a59-42df-ab71-20ef557dfec7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometrySink::AddBeziers
Creates a sequence of cubic Bezier curves and adds them to the geometry sink.  
  
## Syntax  
  
```  
void AddBeziers(  
   const CArray<D2D1_BEZIER_SEGMENT,  
   D2D1_BEZIER_SEGMENT>& beziers  
);  
```  
  
#### Parameters  
 `beziers`  
 An array of Bezier segments that describes the Bezier curves to create. A curve is drawn from the geometry sink's current point (the end point of the last segment drawn or the location specified by BeginFigure) to the end point of the first Bezier segment in the array. if the array contains additional Bezier segments, each subsequent Bezier segment uses the end point of the preceding Bezier segment as its start point.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometrySink Class](../vs140/CD2DGeometrySink-Class.md)