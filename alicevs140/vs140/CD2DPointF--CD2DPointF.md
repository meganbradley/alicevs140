---
title: "CD2DPointF::CD2DPointF"
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
ms.assetid: 915dace3-daaa-4016-955c-46a1f4ff0244
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DPointF::CD2DPointF
Constructs a CD2DPointF object from CPoint object.  
  
## Syntax  
  
```  
CD2DPointF(  
   const CPoint& pt  
);  
CD2DPointF(  
   const D2D1_POINT_2F& pt  
);  
CD2DPointF(  
   const D2D1_POINT_2F* pt  
);  
CD2DPointF(  
   FLOAT fX = 0.,  
   FLOAT fY = 0.  
);  
```  
  
#### Parameters  
 `pt`  
 source point  
  
 `fX`  
 source X  
  
 `fY`  
 source Y  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DPointF Class](../vs140/CD2DPointF-Class.md)