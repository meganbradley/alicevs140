---
title: "CRenderTarget::DrawEllipse"
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
ms.assetid: 4f0788e3-98ef-4e80-afed-92ab6639ccb2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::DrawEllipse
Draws the outline of the specified ellipse using the specified stroke style.  
  
## Syntax  
  
```  
void DrawEllipse(  
   const CD2DEllipse& ellipse,  
   CD2DBrush* pBrush,  
   FLOAT fStrokeWidth = 1.0,  
   ID2D1StrokeStyle* strokeStyle = NULL  
);  
```  
  
#### Parameters  
 `ellipse`  
 The position and radius of the ellipse to draw, in device-independent pixels.  
  
 `pBrush`  
 The brush used to paint the ellipse's outline.  
  
 `fStrokeWidth`  
 The thickness of the ellipse's stroke. The stroke is centered on the ellipse's outline.  
  
 `strokeStyle`  
 The style of stroke to apply to the ellipse's outline, or NULL to paint a solid stroke.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)