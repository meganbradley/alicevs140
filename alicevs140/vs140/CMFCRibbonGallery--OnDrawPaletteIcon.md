---
title: "CMFCRibbonGallery::OnDrawPaletteIcon"
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
ms.assetid: e71ed9e9-45dc-4118-91a6-74f120202213
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::OnDrawPaletteIcon
Called by the framework when a gallery icon is drawn.  
  
## Syntax  
  
```  
virtual void OnDrawPaletteIcon(  
    CDC* pDC,  
    CRect rectIcon,  
    int nIconIndex,  
    CMFCRibbonGalleryIcon* pIcon,  
    COLORREF clrText   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context that is used for drawing.  
  
 [in] `rectIcon`  
 Specifies the bounding rectangle of the icon to draw.  
  
 [in] `nIconIndex`  
 Specifies the zero-based index in the image list of gallery icons of the icon to draw.  
  
 [in] `pIcon`  
 A pointer to the icon being drawn.  
  
 [in] `clrText`  
 Specifies the color for the text of the item to draw.  
  
## Remarks  
 You can override this method in a derived class to customize the appearance of a ribbon gallery.  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)