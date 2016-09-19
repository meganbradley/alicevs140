---
title: "CDC::TransparentBlt"
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
ms.assetid: 225ba60a-943a-434b-ab48-7bcf3955dda7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::TransparentBlt
Call this member function to transfer a bit-block of the color data, which corresponds to a rectangle of pixels from the specified source device context, into a destination device context.  
  
## Syntax  
  
```  
  
      BOOL TransparentBlt(  
   int xDest,  
   int yDest,  
   int nDestWidth,  
   int nDestHeight,  
   CDC* pSrcDC,  
   int xSrc,  
   int ySrc,  
   int nSrcWidth,  
   int nSrcHeight,  
   UINT clrTransparent   
);  
```  
  
#### Parameters  
 `xDest`  
 Specifies the x-coordinate, in logical units, of the upper-left corner of the destination rectangle.  
  
 `yDest`  
 Specifies the y-coordinate, in logical units, of the upper-left corner of the destination rectangle.  
  
 `nDestWidth`  
 Specifies the width, in logical units, of the destination rectangle.  
  
 `nDestHeight`  
 Specifies the height, in logical units, of the destination rectangle.  
  
 `pSrcDC`  
 Pointer to the source device context.  
  
 `xSrc`  
 Specifies the x-coordinate, in logical units, of the source rectangle.  
  
 `ySrc`  
 Specifies the y-coordinate, in logical units, of the source rectangle.  
  
 `nSrcWidth`  
 Specifies the width, in logical units, of the source rectangle.  
  
 `nSrcHeight`  
 Specifies the height, in logical units, of the source rectangle.  
  
 `clrTransparent`  
 The RGB color in the source bitmap to treat as transparent.  
  
## Return Value  
 **TRUE** if successful; otherwise **FALSE**.  
  
## Remarks  
 `TransparentBlt` allows for transparency; that is, the RGB color indicated by `clrTransparent` is rendered transparent for the transfer.  
  
 For more information, see [TransparentBlt](http://msdn.microsoft.com/library/windows/desktop/dd145141) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::AlphaBlend](../vs140/CDC--AlphaBlend.md)   
 [CDC::SetStretchBltMode](../vs140/CDC--SetStretchBltMode.md)