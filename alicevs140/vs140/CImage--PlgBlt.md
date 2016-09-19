---
title: "CImage::PlgBlt"
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
ms.assetid: 6ea1f21d-39d0-48e7-824d-25adf81c8743
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImage::PlgBlt
Performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.  
  
## Syntax  
  
```  
  
      BOOL PlgBlt(  
   HDC hDestDC,  
   const POINT* pPoints,  
   HBITMAP hbmMask = NULL   
) const throw( );  
BOOL PlgBlt(  
   HDC hDestDC,  
   const POINT* pPoints,  
   int xSrc,  
   int ySrc,  
   int nSrcWidth,  
   int nSrcHeight,  
   HBITMAP hbmMask = NULL,  
   int xMask = 0,  
   int yMask = 0   
) const throw( );  
BOOL PlgBlt(  
   HDC hDestDC,  
   const POINT* pPoints,  
   const RECT& rectSrc,  
   HBITMAP hbmMask = NULL,  
   const POINT& pointMask = CPoint(  
   0, 0 )   
) const throw( );  
```  
  
#### Parameters  
 `hDestDC`  
 A handle to the destination device context.  
  
 *pPoints*  
 A pointer to an array of three points in logical space that identify three corners of the destination parallelogram. The upper left corner of the source rectangle is mapped to the first point in this array, the upper-right corner to the second point in this array, and the lower left corner to the third point. The lower-right corner of the source rectangle is mapped to the implicit fourth point in the parallelogram.  
  
 `hbmMask`  
 A handle to an optional monochrome bitmap that is used to mask the colors of the source rectangle.  
  
 `xSrc`  
 The x-coordinate, in logical units, of the upper left corner of the source rectangle.  
  
 `ySrc`  
 The y-coordinate, in logical units, of the upper left corner of the source rectangle.  
  
 `nSrcWidth`  
 The width, in logical units, of the source rectangle.  
  
 `nSrcHeight`  
 The height, in logical units, of the source rectangle.  
  
 `xMask`  
 The x-coordinate of the upper left corner of the monochrome bitmap.  
  
 `yMask`  
 The y-coordinate of the upper left corner of the monochrome bitmap.  
  
 `rectSrc`  
 A reference to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure specifying the coordinates of the source rectangle.  
  
 `pointMask`  
 A [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure indicating the upper left corner of the mask bitmap.  
  
## Return Value  
 Nonzero if successful, otherwise 0.  
  
## Remarks  
 If `hbmMask` identifies a valid monochrome bitmap, **PlgBit** uses this bitmap to mask the bits of color data from the source rectangle.  
  
 This method applies to Windows NT, versions 4.0 and later only. See [PlgBlt](http://msdn.microsoft.com/library/windows/desktop/dd162804) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] and [CImage Limitations with Earlier Operating Systems](../vs140/CImage-Limitations-with-Earlier-Operating-Systems.md) for more detailed information.  
  
## Requirements  
 **Header:** atlimage.h  
  
## See Also  
 [CImage Class](../vs140/CImage-Class.md)   
 [CImage::BitBlt](../vs140/CImage--BitBlt.md)   
 [CImage::MaskBlt](../vs140/CImage--MaskBlt.md)