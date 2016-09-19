---
title: "CD2DPathGeometry::Stream"
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
ms.assetid: 9bcf806b-797e-4c80-98a5-dbf32f2d506c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DPathGeometry::Stream
Copies the contents of the path geometry to the specified ID2D1GeometrySink.  
  
## Syntax  
  
```  
BOOL Stream(  
   ID2D1GeometrySink* geometrySink  
);  
```  
  
#### Parameters  
 `geometrySink`  
 The sink to which the path geometry's contents are copied. Modifying this sink does not change the contents of this path geometry.  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DPathGeometry Class](../vs140/CD2DPathGeometry-Class.md)