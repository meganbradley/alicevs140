---
title: "CMFCRibbonGalleryMenuButton::CMFCRibbonGalleryMenuButton"
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
ms.assetid: b722c08b-1ece-41a0-91d4-29f706f09b43
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGalleryMenuButton::CMFCRibbonGalleryMenuButton
Constructs and initializes a [CMFCRibbonGalleryMenuButton](../vs140/CMFCRibbonGalleryMenuButton-Class.md) object.  
  
## Syntax  
  
```  
CMFCRibbonGalleryMenuButton(  
    UINT uiID,  
    int iImage,  
    LPCTSTR lpszText,  
    CMFCToolBarImages& imagesPalette);  
CMFCRibbonGalleryMenuButton(  
    UINT uiID,  
    int iImage,  
    LPCTSTR lpszText,  
    UINT uiImagesPaletteResID = 0,  
    int cxPaletteImage = 0);  
```  
  
#### Parameters  
 `uiID`  
 The command ID of the button. This is the value sent in the **WM_COMMAND** message when the user clicks this button.  
  
 `iImage`  
 The index of the image to display with the gallery menu button. The images are stored in the `imagesPalette` parameter.  
  
 `lpszText`  
 The text to display on the menu button.  
  
 `imagesPalette`  
 Contains the list of images to display on the gallery.  
  
 `uiImagesPaletteResID`  
 The resource ID of the image list for the images to display on the gallery.  
  
 `cxPaletteImage`  
 Specifies the width in pixels of the image to display on the gallery.  
  
## Remarks  
 The gallery menu button is displayed as a pop-up menu that has an arrow. When the user clicks this button, a gallery of images is displayed.  
  
## Example  
 The following example demonstrates how to use the constructor of the `CMFCRibbonGalleryMenuButton` class. This code snippet is part of the [MS Office 2007 Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MSOffice2007Demo#8](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MSOffice2007Demo#8)]  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGalleryMenuButton Class](../vs140/CMFCRibbonGalleryMenuButton-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)