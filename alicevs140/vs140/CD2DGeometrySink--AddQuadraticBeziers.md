---
title: "CD2DGeometrySink::AddQuadraticBeziers"
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
ms.assetid: faf7535d-fea7-44d3-85c6-cafe6477d811
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometrySink::AddQuadraticBeziers
Adds a sequence of quadratic Bezier segments as an array in a single call.  
  
## Syntax  
  
```  
void AddQuadraticBeziers(  
   const CArray<D2D1_QUADRATIC_BEZIER_SEGMENT,  
   D2D1_QUADRATIC_BEZIER_SEGMENT>& beziers  
);  
```  
  
#### Parameters  
 `beziers`  
 An array of a sequence of quadratic Bezier segments.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometrySink Class](../vs140/CD2DGeometrySink-Class.md)