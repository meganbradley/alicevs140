---
title: "AfxDrawDitheredBitmap"
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
ms.topic: article
ms.assetid: b41e9c4b-b567-4e3c-b8e0-b45e9dd1a7a3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxDrawDitheredBitmap
Draws a bitmap, replacing its background with a dithered (checker) pattern.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxDrawDitheredBitmap(  
   CDC *pDC,  
   int x,  
   int y,  
   const CBitmap &rSrc,  
   COLORREF cr1,  
   COLORREF cr2  
);  
```  
  
#### Parameters  
 `pDC`  
 Points to the destination DC.  
  
 *x*  
 The destination x-coordinate.  
  
 *y*  
 The destination y-coordinate.  
  
 `rSrc`  
 The source bitmap.  
  
 `cr1`  
 One of the two dither colors, typically white.  
  
 `cr2`  
 The other dither color, typically light gray (COLOR_MENU).  
  
## Remarks  
 The source bitmap is drawn on the destination DC with a two-color (`cr1` and `cr2`) checkered pattern replacing the bitmap's background. The background of the source bitmap is defined as its white pixels and all pixels matching the color of the pixel in the upper-left corner of the bitmap.  
  
 ![Comparison of dithered and original icon versions](../vs140/media/vcDitheredBitmap.gif "vcDitheredBitmap")  
  
## Example  
 [!CODE [NVC_MFCDocView#190](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#190)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Gray and Dithered Bitmap Functions](../vs140/Gray-and-Dithered-Bitmap-Functions.md)   
 [AfxGetDitheredBitmap](../vs140/AfxGetDitheredBitmap.md)   
 [AfxDrawGrayBitmap](../vs140/AfxDrawGrayBitmap.md)