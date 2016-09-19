---
title: "CImage::BitBlt"
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
ms.assetid: 0c84bf85-7b09-40ea-8e27-06672d917a64
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::BitBlt
Copies a bitmap from the source device context to this current device context.  
  
## Syntax  
  
```  
  
      BOOL BitBlt(  
   HDC hDestDC,  
   int xDest,  
   int yDest,  
   DWORD dwROP = SRCCOPY   
) const throw( );  
BOOL BitBlt(  
   HDC hDestDC,  
   const POINT& pointDest,  
   DWORD dwROP = SRCCOPY   
) const throw( );  
BOOL BitBlt(  
   HDC hDestDC,  
   int xDest,  
   int yDest,  
   int nDestWidth,  
   int nDestHeight,  
   int xSrc,  
   int ySrc,  
   DWORD dwROP = SRCCOPY   
) const throw( );  
BOOL BitBlt(  
   HDC hDestDC,  
   const RECT& rectDest,  
   const POINT& pointSrc,  
   DWORD dwROP = SRCCOPY   
) const throw( );  
```  
  
#### Parameters  
 `hDestDC`  
 The destination **HDC**.  
  
 `xDest`  
 The logical x-coordinate of the upper left corner of the destination rectangle.  
  
 `yDest`  
 The logical y-coordinate of the upper left corner of the destination rectangle.  
  
 `dwROP`  
 The raster operation to be performed. Raster-operation codes define exactly how to combine the bits of the source, the destination, and the pattern (as defined by the currently selected brush) to form the destination. See [BitBlt](http://msdn.microsoft.com/library/windows/desktop/dd183370) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a list of other raster-operation codes and their descriptions.  
  
 `pointDest`  
 A [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure indicating the upper left corner of the destination rectangle.  
  
 `nDestWidth`  
 The width, in logical units, of the destination rectangle.  
  
 `nDestHeight`  
 The height, in logical units, of the destination rectangle.  
  
 `xSrc`  
 The logical x-coordinate of the upper left corner of the source rectangle.  
  
 `ySrc`  
 The logical y-coordinate of the upper left corner of the source rectangle.  
  
 `rectDest`  
 A [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure indicating the destination rectangle.  
  
 `pointSrc`  
 A **POINT** structure indicating the upper left corner of the source rectangle.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 For more information, see [BitBlt](http://msdn.microsoft.com/library/windows/desktop/dd183370) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::PlgBlt](../vs140/CImage--PlgBlt.md)   
 [CImage::StretchBlt](../vs140/CImage--StretchBlt.md)   
 [CImage::MaskBlt](../vs140/CImage--MaskBlt.md)