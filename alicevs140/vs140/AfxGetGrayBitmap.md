---
title: "AfxGetGrayBitmap"
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
ms.assetid: 4f48b35e-c6d5-4f3f-a86a-b5979f965b1b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetGrayBitmap
Copies a gray version of a bitmap.  
  
## Syntax  
  
```  
  
      void AFXAPI AfxGetGrayBitmap(  
   const CBitmap &rSrc,  
   CBitmap *pDest,  
   COLORREF crBackground  
);  
```  
  
#### Parameters  
 `rSrc`  
 The source bitmap.  
  
 `pDest`  
 The destination bitmap.  
  
 `crBackground`  
 The new background color (typically gray, such as COLOR_MENU).  
  
## Remarks  
 A bitmap copied with `AfxGetGrayBitmap` will have the appearance of a disabled control.  
  
 ![Comparison of gray and original icon versions](../vs140/media/vcGrayBitmap.gif "vcGrayBitmap")  
  
## Example  
 [!CODE [NVC_MFCDocView#193](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#193)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Gray and Dithered Bitmap Functions](../vs140/Gray-and-Dithered-Bitmap-Functions.md)   
 [AfxDrawGrayBitmap](../vs140/AfxDrawGrayBitmap.md)   
 [AfxGetDitheredBitmap](../vs140/AfxGetDitheredBitmap.md)