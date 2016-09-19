---
title: "CDrawingManager::SetAlphaPixel"
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
ms.assetid: 15631f6b-e0cc-41ab-af89-a46be6cd281d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::SetAlphaPixel
Colors a transparent pixel in a bitmap.  
  
## Syntax  
  
```  
static void __stdcall SetAlphaPixel(  
   COLORREF* pBits,  
   CRect rect,  
   int x,  
   int y,  
   int percent,  
   int iShadowSize,  
   COLORREF clrBase = (COLORREF)-1,  
   BOOL bIsRight = TRUE  
);  
```  
  
#### Parameters  
 [in] `pBits`  
 A pointer to the bit values for the bitmap.  
  
 [in] `rect`  
 A rectangular area in your application. The drawing manager draws a shadow underneath and to the right of this area.  
  
 [in] `x`  
 The horizontal coordinate of the pixel to color.  
  
 [in] `y`  
 The vertical coordinate of the pixel to color.  
  
 [in] `percent`  
 The percentage of transparency.  
  
 [in] `iShadowSize`  
 The width and height of the shadow.  
  
 [in] `clrBase`  
 The color of the shadow.  
  
 [in] `bIsRight`  
 A Boolean parameter that indicates which pixel to color. See the Remarks section for more information.  
  
## Remarks  
 This method is a helper method that is used by the [CDrawingManager::DrawShadow](../vs140/CDrawingManager--DrawShadow.md) method. We recommend that if you want to draw a shadow, call `CDrawingManager::DrawShadow` instead.  
  
 If `bIsRight` is set to `TRUE`, the pixel to color is measured `x` pixels from the right edge of `rect`. If it is `FALSE`, the pixel to color is measured `x` pixels from the left edge of `rect`.  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CDrawingManager::DrawShadow](../vs140/CDrawingManager--DrawShadow.md)