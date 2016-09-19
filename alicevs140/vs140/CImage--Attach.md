---
title: "CImage::Attach"
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
ms.assetid: b59a23a9-bcf4-4e34-95c7-e0024a4cdf4c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::Attach
Attaches `hBitmap` to a `CImage` object.  
  
## Syntax  
  
```  
  
      void Attach(  
   HBITMAP hBitmap,   
   DIBOrientation eOrientation = DIBOR_DEFAULT  
) throw();  
```  
  
#### Parameters  
 `hBitmap`  
 A handle to an `HBITMAP`.  
  
 *eOrientation*  
 Specifies the orientation of the bitmap. Can be one of the following:  
  
-   **DIBOR_DEFAULT** The orientation of the bitmap is determined by the operating system. However, this may not always have the intended results on all operating systems. For more information on this, see the following Knowledge Base article (**Q186586**): PRB: GetObject() Always Returns Positive Height For DIB Sections.  
  
-   **DIBOR_BOTTOMUP** The lines of the bitmap are in reverse order. This causes [CImage::GetBits](../vs140/CImage--GetBits.md) to return a pointer near the end of the bitmap buffer and [CImage::GetPitch](../vs140/CImage--GetPitch.md) to return a negative number.  
  
-   **DIBOR_TOPDOWN**  The lines of the bitmap are in top to bottom order. This causes [CImage::GetBits](../vs140/CImage--GetBits.md) to return a pointer to the first byte of the bitmap buffer and [CImage::GetPitch](../vs140/CImage--GetPitch.md) to return a positive number.  
  
## Remarks  
 The bitmap can be either a non-DIB section bitmap or a DIB section bitmap. See [IsDIBSection](../vs140/CImage--IsDIBSection.md) for a list of methods that you can use only with DIB section bitmaps.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::CImage](../vs140/CImage--CImage.md)