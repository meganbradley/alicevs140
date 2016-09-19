---
title: "CD2DRectU::CD2DRectU"
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
ms.assetid: c88d569c-bdfc-4c19-94fd-018b0ff435df
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CD2DRectU::CD2DRectU
Constructs a CD2DRectU object from CRect object.  
  
## Syntax  
  
```  
CD2DRectU(  
   const CRect& rect  
);  
CD2DRectU(  
   const D2D1_RECT_U& rect  
);  
CD2DRectU(  
   const D2D1_RECT_U* rect  
);  
CD2DRectU(  
   UINT32 uLeft = 0,  
   UINT32 uTop = 0,  
   UINT32 uRight = 0,  
   UINT32 uBottom = 0  
);  
```  
  
#### Parameters  
 `rect`  
 source rectangle  
  
 `uLeft`  
 source left coordinate  
  
 `uTop`  
 source top coordinate  
  
 `uRight`  
 source right coordinate  
  
 `uBottom`  
 source bottom coordinate  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CD2DRectU Class](../vs140/CD2DRectU-Class.md)