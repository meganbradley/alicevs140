---
title: "CD2DGeometry::GetWidenedBounds"
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
ms.assetid: 15cc5483-0a08-4940-946a-87165eee0e3f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometry::GetWidenedBounds
Gets the bounds of the geometry after it has been widened by the specified stroke width and style and transformed by the specified matrix.  
  
## Syntax  
  
```  
BOOL GetWidenedBounds(  
   FLOAT strokeWidth,  
   ID2D1StrokeStyle* strokeStyle,  
   const D2D1_MATRIX_3X2_F& worldTransform,  
   CD2DRectF& bounds,  
   FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE  
) const;  
```  
  
#### Parameters  
 `strokeWidth`  
 The amount by which to widen the geometry by stroking its outline.  
  
 `strokeStyle`  
 The style of the stroke that widens the geometry.  
  
 `worldTransform`  
 A transform to apply to the geometry after the geometry is transformed and after the geometry has been stroked.  
  
 `bounds`  
 When this method returns, contains the bounds of the widened geometry. You must allocate storage for this parameter.  
  
 `flatteningTolerance`  
 The maximum bounds on the distance between points in the polygonal approximation of the geometries. Smaller values produce more accurate results but cause slower execution.  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometry Class](../vs140/CD2DGeometry-Class.md)