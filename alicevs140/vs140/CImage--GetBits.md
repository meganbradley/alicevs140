---
title: "CImage::GetBits"
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
ms.assetid: 48e842f6-cffa-4e61-8259-e8255a31739c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetBits
Retrieves a pointer to the actual bit values of a given pixel in a bitmap.  
  
## Syntax  
  
```  
  
void* GetBits( ) throw( );  
  
```  
  
## Return Value  
 A pointer to the bitmap buffer. If the bitmap is a bottom-up DIB, the pointer points near the end of the buffer. If the bitmap is a top-down DIB, the pointer points to the first byte of the buffer.  
  
## Remarks  
 Using this pointer, along with the value returned by [GetPitch](../vs140/CImage--GetPitch.md), you can locate and change individual pixels in an image.  
  
> [!NOTE]
>  This method supports only DIB section bitmaps; consequently, you access the pixels of a `CImage` object the same way you would the pixels of a DIB section. The returned pointer points to the pixel at the location (0, 0).  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [Device-Independent Bitmaps](http://msdn.microsoft.com/library/windows/desktop/dd183562)   
 [GetDIBits](http://msdn.microsoft.com/library/windows/desktop/dd144879)   
 [CImage::GetBPP](../vs140/CImage--GetBPP.md)   
 [CImage::GetDC](../vs140/CImage--GetDC.md)