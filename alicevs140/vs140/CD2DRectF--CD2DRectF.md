---
title: "CD2DRectF::CD2DRectF"
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
ms.assetid: 2463814c-35f4-431e-bdac-e3e9204c8e1d
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DRectF::CD2DRectF
Constructs a CD2DRectF object from CRect object.  
  
## Syntax  
  
```  
CD2DRectF(  
   const CRect& rect  
);  
CD2DRectF(  
   const D2D1_RECT_F& rect  
);  
CD2DRectF(  
   const D2D1_RECT_F* rect  
);  
CD2DRectF(  
   FLOAT fLeft = 0.,  
   FLOAT fTop = 0.,  
   FLOAT fRight = 0.,  
   FLOAT fBottom = 0.  
);  
```  
  
#### Parameters  
 `rect`  
 source rectangle  
  
 `fLeft`  
 source left coordinate  
  
 `fTop`  
 source top coordinate  
  
 `fRight`  
 source right coordinate  
  
 `fBottom`  
 source bottom coordinate  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DRectF Class](../vs140/CD2DRectF-Class.md)