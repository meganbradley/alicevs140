---
title: "CD2DGeometrySink::SetFillMode"
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
ms.assetid: 145e04f0-995c-4e6e-9e1c-232d5aa8919f
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometrySink::SetFillMode
Specifies the method used to determine which points are inside the geometry described by this geometry sink and which points are outside.  
  
## Syntax  
  
```  
void SetFillMode(  
   D2D1_FILL_MODE fillMode  
);  
```  
  
#### Parameters  
 `fillMode`  
 The method used to determine whether a given point is part of the geometry.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometrySink Class](../vs140/CD2DGeometrySink-Class.md)