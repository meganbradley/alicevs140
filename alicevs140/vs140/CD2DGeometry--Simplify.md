---
title: "CD2DGeometry::Simplify"
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
ms.assetid: 8cd2a0fa-c1a1-44cd-adb8-7396e0db1851
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometry::Simplify
Creates a simplified version of the geometry that contains only lines and (optionally) cubic Bezier curves and writes the result to an ID2D1SimplifiedGeometrySink.  
  
## Syntax  
  
```  
BOOL Simplify(  
   D2D1_GEOMETRY_SIMPLIFICATION_OPTION simplificationOption,  
   const D2D1_MATRIX_3X2_F& worldTransform,  
   ID2D1SimplifiedGeometrySink* geometrySink,  
   FLOAT flatteningTolerance = D2D1_DEFAULT_FLATTENING_TOLERANCE  
) const;  
```  
  
#### Parameters  
 `simplificationOption`  
 A value that specifies whether the simplified geometry should contain curves.  
  
 `worldTransform`  
 The transform to apply to the simplified geometry.  
  
 `geometrySink`  
 The ID2D1SimplifiedGeometrySink to which the simplified geometry is appended.  
  
 `flatteningTolerance`  
 The maximum bounds on the distance between points in the polygonal approximation of the geometry. Smaller values produce more accurate results but cause slower execution.  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometry Class](../vs140/CD2DGeometry-Class.md)