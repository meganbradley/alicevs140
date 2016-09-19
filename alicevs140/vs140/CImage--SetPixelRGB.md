---
title: "CImage::SetPixelRGB"
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
ms.assetid: 9a711cac-c3b2-44d8-8817-8962bdc2e46a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::SetPixelRGB
Sets the pixel at the locations specified by *x* and *y* to the colors indicated by *r*, *g*, and *b*, in a red, green, blue (RGB) image.  
  
## Syntax  
  
```  
  
      void SetPixelRGB(  
   int x,  
   int y,  
   BYTE r,  
   BYTE g,  
   BYTE b   
) throw( );  
```  
  
#### Parameters  
 *x*  
 The horizontal location of the pixel to set.  
  
 *y*  
 The vertical location of the pixel to set.  
  
 *r*  
 The intensity of the red color.  
  
 *g*  
 The intensity of the green color.  
  
 *b*  
 The intensity of the blue color.  
  
## Remarks  
 The red, green, and blue parameters are each represented by a number between 0 and 255. If you set all three parameters to zero, the combined resulting color is black. If you set all three parameters to 255, the combined resulting color is white.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::SetPixel](../vs140/CImage--SetPixel.md)   
 [CImage::SetPixelIndexed](../vs140/CImage--SetPixelIndexed.md)