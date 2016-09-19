---
title: "CRenderTarget::DrawGlyphRun"
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
ms.assetid: 1a08172d-076a-416c-982a-be9355e544aa
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::DrawGlyphRun
Draws the specified glyphs.  
  
## Syntax  
  
```  
void DrawGlyphRun(  
   const CD2DPointF& ptBaseLineOrigin,  
   const DWRITE_GLYPH_RUN& glyphRun,  
   CD2DBrush* pForegroundBrush,  
   DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL  
);  
```  
  
#### Parameters  
 `ptBaseLineOrigin`  
 The origin, in device-independent pixels, of the glyphs' baseline.  
  
 `glyphRun`  
 The glyphs to render.  
  
 `pForegroundBrush`  
 The brush used to paint the specified glyphs.  
  
 `measuringMode`  
 A value that indicates how glyph metrics are used to measure text when it is formatted. The default value is DWRITE_MEASURING_MODE_NATURAL.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)