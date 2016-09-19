---
title: "CD2DEllipse::CD2DEllipse"
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
ms.assetid: e170f860-51b0-4e1a-8793-fa685d474349
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DEllipse::CD2DEllipse
Constructs a CD2DEllipse object from CD2DRectF object.  
  
## Syntax  
  
```  
CD2DEllipse(  
   const CD2DRectF& rect  
);  
CD2DEllipse(  
   const D2D1_ELLIPSE& ellipse  
);  
CD2DEllipse(  
   const D2D1_ELLIPSE* ellipse  
);  
CD2DEllipse(  
   const CD2DPointF& ptCenter,  
   const CD2DSizeF& sizeRadius  
);  
```  
  
#### Parameters  
 `rect`  
 source rectangle  
  
 `ellipse`  
 source ellipse  
  
 `ptCenter`  
 The center point of the ellipse.  
  
 `sizeRadius`  
 The X-radius and Y-radius of the ellipse.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DEllipse Class](../vs140/CD2DEllipse-Class.md)