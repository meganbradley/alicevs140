---
title: "CD2DGeometrySink::EndFigure"
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
ms.assetid: 2c2d7190-e7a4-4069-a34a-1cd6b21c24be
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DGeometrySink::EndFigure
Ends the current figure; optionally, closes it.  
  
## Syntax  
  
```  
void EndFigure(  
   D2D1_FIGURE_END figureEnd  
);  
```  
  
#### Parameters  
 `figureEnd`  
 A value that indicates whether the current figure is closed. If the figure is closed, a line is drawn between the current point and the start point specified by BeginFigure.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DGeometrySink Class](../vs140/CD2DGeometrySink-Class.md)