---
title: "CImage::GetPixel"
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
ms.assetid: 483aa392-57d8-4ecd-85b4-7818a231fe69
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetPixel
Retrieves the color of the pixel at the location specified by *x* and *y*.  
  
## Syntax  
  
```  
  
      COLORREF GetPixel(  
   int x,  
   int y   
) const throw( );  
```  
  
#### Parameters  
 *x*  
 The x-coordinate of the pixel.  
  
 *y*  
 The y-coordinate of the pixel.  
  
## Return Value  
 The red, green, blue (RGB) value of the pixel. If the pixel is outside of the current clipping region, the return value is **CLR_INVALID**.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetPixelAddress](../vs140/CImage--GetPixelAddress.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)