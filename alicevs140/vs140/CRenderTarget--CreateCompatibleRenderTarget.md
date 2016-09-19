---
title: "CRenderTarget::CreateCompatibleRenderTarget"
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
ms.assetid: 8d5a155f-a27b-48ac-8e6d-e716360737db
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRenderTarget::CreateCompatibleRenderTarget
Creates a new bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target .  
  
## Syntax  
  
```  
BOOL CreateCompatibleRenderTarget(  
   CBitmapRenderTarget& bitmapTarget,  
   CD2DSizeF sizeDesired = CD2DSizeF(0.,  
   0.),  
   CD2DSizeU sizePixelDesired = CD2DSizeU(0,  
   0),  
   D2D1_PIXEL_FORMAT* desiredFormat = NULL,  
   D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS options = D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE  
);  
```  
  
#### Parameters  
 `bitmapTarget`  
 When this method returns, contains the address of a pointer to a new bitmap render target. This parameter is passed uninitialized.  
  
 `sizeDesired`  
 The desired size of the new render target in device-independent pixels if it should be different from the original render target, or NULL. For more information, see the Remarks section.  
  
 `sizePixelDesired`  
 The desired size of the new render target in pixels if it should be different from the original render target, or NULL. For more information, see the Remarks section.  
  
 `desiredFormat`  
 The desired pixel format and alpha mode of the new render target, or NULL. If the pixel format is set to DXGI_FORMAT_UNKNOWN or if this parameter is null, the new render target uses the same pixel format as the original render target. If the alpha mode is D2D1_ALPHA_MODE_UNKNOWN or this parameter is NULL, the alpha mode of the new render target defaults to D2D1_ALPHA_MODE_PREMULTIPLIED. For information about supported pixel formats, see Supported Pixel Formats and Alpha Modes.  
  
 `options`  
 A value that specifies whether the new render target must be compatible with GDI.  
  
## Return Value  
 If the method succeeds, it returns TRUE. Otherwise, it returns FALSE.  
  
## Requirements  
 **Header:** afxrendertarget.h  
  
## See Also  
 [CRenderTarget Class](../vs140/CRenderTarget-Class.md)