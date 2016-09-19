---
title: "CMFCRibbonGallery::SetPalette"
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
ms.assetid: 5643f6c7-ef89-4a72-9b13-45ca33bcea31
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::SetPalette
Attaches a palette to a ribbon gallery.  
  
## Syntax  
  
```  
void SetPalette(  
    CMFCToolBarImages& imagesPalette   
);  
void SetPalette(  
    UINT uiImagesPaletteResID,  
    int cxPaletteImage   
);  
```  
  
#### Parameters  
 [in] `imagesPalette`  
 Specifies the image list that contains the icons to appear on the gallery.  
  
 [in] `uiImagesPaletteResID`  
 Specifies the resource ID of the image list that contains the icons to appear on the gallery.  
  
 [in] `cxPaletteImage`  
 Specifies the width, in pixels, of an image on the gallery.  
  
## Remarks  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)