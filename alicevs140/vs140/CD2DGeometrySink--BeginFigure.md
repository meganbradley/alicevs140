---
title: "CD2DGeometrySink::BeginFigure"
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
ms.assetid: f2cb19d5-2ec4-4a9e-9a52-3960fd6ecf78
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometrySink::BeginFigure
Starts a new figure at the specified point.  
  
## Syntax  
  
```  
void BeginFigure(  
   CD2DPointF startPoint,  
   D2D1_FIGURE_BEGIN figureBegin  
);  
```  
  
#### Parameters  
 `startPoint`  
 The point at which to begin the new figure.  
  
 `figureBegin`  
 Whether the new figure should be hollow or filled.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometrySink Class](../vs140/CD2DGeometrySink-Class.md)