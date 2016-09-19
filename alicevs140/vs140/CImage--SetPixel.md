---
title: "CImage::SetPixel"
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
ms.assetid: 0f3ec0bb-6d9d-4379-bcfd-f4d97c2d29ae
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::SetPixel
Sets the color of a pixel at a given location in the bitmap.  
  
## Syntax  
  
```  
  
      void SetPixel(  
   int x,  
   int y,  
   COLORREF color   
) throw( );  
```  
  
#### Parameters  
 *x*  
 The horizontal location of the pixel to set.  
  
 *y*  
 The vertical location of the pixel to set.  
  
 `color`  
 The color to which you set the pixel.  
  
## Remarks  
 This method fails if the pixel coordinates lie outside of the selected clipping region.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetPixel](../vs140/CImage--GetPixel.md)   
 [CImage::SetPixelIndexed](../vs140/CImage--SetPixelIndexed.md)   
 [CImage::SetPixelRGB](../vs140/CImage--SetPixelRGB.md)