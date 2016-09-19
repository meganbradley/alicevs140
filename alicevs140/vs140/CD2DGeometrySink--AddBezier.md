---
title: "CD2DGeometrySink::AddBezier"
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
ms.assetid: 4bd67cb2-6dd6-4e3f-a3cb-33dd72b11c36
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometrySink::AddBezier
Creates a cubic Bezier curve between the current point and the specified end point.  
  
## Syntax  
  
```  
void AddBezier(  
   const D2D1_BEZIER_SEGMENT& bezier  
);  
```  
  
#### Parameters  
 `bezier`  
 A structure that describes the control points and end point of the Bezier curve to add.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometrySink Class](../vs140/CD2DGeometrySink-Class.md)