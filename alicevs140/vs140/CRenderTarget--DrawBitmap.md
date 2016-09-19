---
title: "CRenderTarget::DrawBitmap"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: aff287cf-db8b-4f6d-b381-59160133e3df
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::DrawBitmap
Draws the formatted text described by the specified IDWriteTextLayout object.  
  
## Syntax  
  
```  
void DrawBitmap(  
   CD2DBitmap* pBitmap,  
   const CD2DRectF& rectDest,  
   float fOpacity = 1.0,  
   D2D1_BITMAP_INTERPOLATION_MODE interpolationMode = D2D1_BITMAP_INTERPOLATION_MODE_LINEAR,  
   const CD2DRectF* pRectSrc = NULL  
);  
```  
  
#### Parameters  
 `pBitmap`  
 The bitmap to render.  
  
 `rectDest`  
 The size and position, in device-independent pixels in the render target's coordinate space, of the area to which the bitmap is drawn. If the rectangle is not well-ordered, nothing is drawn, but the render target does not enter an error state.  
  
 `fOpacity`  
 A value between 0.0f and 1.0f, inclusive, that specifies an opacity value to apply to the bitmap; this value is multiplied against the alpha values of the bitmap's contents.  
  
 `interpolationMode`  
 The interpolation mode to use if the bitmap is scaled or rotated by the drawing operation.  
  
 `pRectSrc`  
 The size and position, in device-independent pixels in the bitmap's coordinate space, of the area within the bitmap to draw.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)