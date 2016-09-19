---
title: "CImage::GetPitch"
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
ms.assetid: 9756ad0b-904f-48ba-b7bd-5a56662362cb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::GetPitch
Retrieves the pitch of an image.  
  
## Syntax  
  
```  
  
int GetPitch( ) const throw( );  
  
```  
  
## Return Value  
 The pitch of the image. If the return value is negative, the bitmap is a bottom-up DIB and its origin is the lower left corner. If the return value is positive, the bitmap is a top-down DIB and its origin is the upper left corner.  
  
## Remarks  
 The pitch is the distance, in bytes, between two memory addresses that represent the beginning of one bitmap line and the beginning of the next bitmap line. Because pitch is measured in bytes, the pitch of an image helps you to determine the pixel format. The pitch can also include additional memory, reserved for the bitmap.  
  
 Use `GetPitch` with [GetBits](../vs140/CImage--GetBits.md) to find individual pixels of an image.  
  
> [!NOTE]
>  This method supports only DIB section bitmaps.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::GetPixelAddress](../vs140/CImage--GetPixelAddress.md)   
 [CImage::GetWidth](../vs140/CImage--GetWidth.md)   
 [CImage::GetHeight](../vs140/CImage--GetHeight.md)