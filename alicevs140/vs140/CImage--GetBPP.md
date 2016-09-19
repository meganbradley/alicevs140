---
title: "CImage::GetBPP"
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
ms.assetid: 91031668-bf3c-4bd4-8b1a-984805f8c8d6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetBPP
Retrieves the bits-per-pixel value.  
  
## Syntax  
  
```  
  
int GetBPP( ) const throw( );  
  
```  
  
## Return Value  
 The number of bits per pixel.  
  
## Remarks  
 This value determines the number of bits that define each pixel and the maximum number of colors in the bitmap.  
  
 The bits per pixel is usually 1, 4, 8, 16, 24, or 32. See the **biBitCount** member of [BITMAPINFOHEADER](http://msdn.microsoft.com/library/windows/desktop/dd183376) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more information about this value.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetPixelAddress](../vs140/CImage--GetPixelAddress.md)   
 [CImage::GetBits](../vs140/CImage--GetBits.md)   
 [CImage::GetDC](../vs140/CImage--GetDC.md)