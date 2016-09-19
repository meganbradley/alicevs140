---
title: "CImage::GetPixelAddress"
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
ms.assetid: 8b65af22-3986-4e23-9513-ac1cd708238e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetPixelAddress
Retrieves the exact address of a pixel.  
  
## Syntax  
  
```  
  
      void* GetPixelAddress(  
   int x,  
   int y   
) throw( );  
```  
  
#### Parameters  
 *x*  
 The x-coordinate of the pixel.  
  
 *y*  
 The y-coordinate of the pixel.  
  
## Remarks  
 The address is determined according to the coordinates of a pixel, the pitch of the bitmap, and the bits per pixel.  
  
 For formats that have less than 8 bits per pixel, this method returns the address of the byte containing the pixel. For example, if your image format has 4 bits per pixel, `GetPixelAddress` returns the address of the first pixel in the byte, and you must calculate for 2 pixels per byte.  
  
> [!NOTE]
>  This method supports only DIB section bitmaps.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)