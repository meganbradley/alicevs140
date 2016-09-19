---
title: "CRenderTarget::FillGeometry"
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
ms.assetid: 0405163c-856a-4125-a2f3-cce50d3f32ba
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::FillGeometry
Paints the interior of the specified geometry.  
  
## Syntax  
  
```  
void FillGeometry(  
   CD2DGeometry* pGeometry,  
   CD2DBrush* pBrush,  
   CD2DBrush* pOpacityBrush = NULL  
);  
```  
  
#### Parameters  
 `pGeometry`  
 The geometry to paint.  
  
 `pBrush`  
 The brush used to paint the geometry's interior.  
  
 `pOpacityBrush`  
 The opacity mask to apply to the geometry;NULL for no opacity mask. If an opacity mask (the opacityBrush parameter) is specified, brush must be an ID2D1BitmapBrush that has its x- and y-extend modes set to D2D1_EXTEND_MODE_CLAMP. For more information, see the Remarks section.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)