---
title: "AfxGetDitheredBitmap"
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
ms.assetid: 3eb418a2-7473-4580-a2d9-cfa287fd69d5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetDitheredBitmap
Copies a bitmap, replacing its background with a dithered (checker) pattern.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxGetDitheredBitmap(  
   const CBitmap &rSrc,  
   CBitmap *pDest,  
   COLORREF cr1,  
   COLORREF cr2  
);  
```  
  
#### Parameters  
 `rSrc`  
 The source bitmap.  
  
 `pDest`  
 The destination bitmap.  
  
 `cr1`  
 One of the two dither colors, typically white.  
  
 `cr2`  
 The other dither color, typically light gray (COLOR_MENU).  
  
## Remarks  
 The source bitmap is copied to the destination bitmap with a two-color (`cr1` and `cr2`) checkered pattern replacing the source bitmap's background. The background of the source bitmap is defined as its white pixels and all pixels matching the color of the pixel in the upper-left corner of the bitmap.  
  
 ![Comparison of dithered and original icon versions](../vs140/media/vcDitheredBitmap.gif "vcDitheredBitmap")  
  
## Example  
 [!CODE [NVC_MFCDocView#192](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#192)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Gray and Dithered Bitmap Functions](../vs140/Gray-and-Dithered-Bitmap-Functions.md)   
 [AfxDrawDitheredBitmap](../vs140/AfxDrawDitheredBitmap.md)   
 [AfxGetGrayBitmap](../vs140/AfxGetGrayBitmap.md)