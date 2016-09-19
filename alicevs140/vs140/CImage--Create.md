---
title: "CImage::Create"
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
ms.assetid: 447f4ebf-5cf4-4862-ab4c-ee643c78c717
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::Create
Creates a `CImage` bitmap and attach it to the previously constructed `CImage` object.  
  
## Syntax  
  
```  
  
      BOOL Create(  
   int nWidth,  
   int nHeight,  
   int nBPP,  
   DWORD dwFlags = 0   
) throw( );  
```  
  
#### Parameters  
 `nWidth`  
 The width of the `CImage` bitmap, in pixels.  
  
 `nHeight`  
 The height of the `CImage` bitmap, in pixels. If `nHeight` is positive, the bitmap is a bottom-up DIB and its origin is the lower left corner. If `nHeight` is negative, the bitmap is a top-down DIB and its origin is the upper left corner.  
  
 `nBPP`  
 The numbers of bits per pixel in the bitmap. Usually 4, 8, 16, 24, or 32. Can be 1 for monochrome bitmaps or masks.  
  
 `dwFlags`  
 Specifies if the bitmap object has an alpha channel. Can be a combination of zero or more of the following values:  
  
-   **createAlphaChannel** Can only be used if `nBPP` is 32, and `eCompression` is **BI_RGB**. If specified, the created image has an alpha (transparency) value for each pixel, stored in the 4th byte of each pixel (unused in a non-alpha 32-bit image). This alpha channel is automatically used when calling [CImage::AlphaBlend](../vs140/CImage--AlphaBlend.md).  
  
> [!NOTE]
>  In calls to [CImage::Draw](../vs140/CImage--Draw.md), images with an alpha channel are automatically alpha blended to the destination.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::CImage](../vs140/CImage--CImage.md)   
 [CImage::AlphaBlend](../vs140/CImage--AlphaBlend.md)   
 [CImage::CreateEx](../vs140/CImage--CreateEx.md)