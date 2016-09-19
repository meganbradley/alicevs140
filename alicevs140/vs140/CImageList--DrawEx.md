---
title: "CImageList::DrawEx"
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
ms.assetid: 65b63d87-0fad-46d1-a207-ea6b9915dfa0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::DrawEx
Draws an image list item in the specified device context.  
  
## Syntax  
  
```  
  
      BOOL DrawEx(  
   CDC* pDC,  
   int nImage,  
   POINT pt,  
   SIZE sz,  
   COLORREF clrBk,  
   COLORREF clrFg,  
   UINT nStyle   
);  
```  
  
#### Parameters  
 `pDC`  
 Pointer to the destination device context.  
  
 `nImage`  
 Zero-based index of the image to draw.  
  
 `pt`  
 Location at which to draw within the specified device context.  
  
 `sz`  
 Size of the portion of the image to draw relative to the upper-left corner of the image. See `dx` and *dy* in [ImageList_DrawEx](http://msdn.microsoft.com/library/windows/desktop/bb761536) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 *clrBk*  
 Background color of the image. See *rgbBk* in [ImageList_DrawEx](http://msdn.microsoft.com/library/windows/desktop/bb761536) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 *clrFg*  
 Foreground color of the image. See *rgbFg* in [ImageList_DrawEx](http://msdn.microsoft.com/library/windows/desktop/bb761536) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 `nStyle`  
 Flag specifying the drawing style. See *fStyle* in [ImageList_DrawEx](http://msdn.microsoft.com/library/windows/desktop/bb761536) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The function uses the specified drawing style and blends the image with the specified color.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#10)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::BeginDrag](../vs140/CImageList--BeginDrag.md)   
 [CImageList::EndDrag](../vs140/CImageList--EndDrag.md)   
 [CImageList::DragMove](../vs140/CImageList--DragMove.md)   
 [CImageList::Draw](../vs140/CImageList--Draw.md)