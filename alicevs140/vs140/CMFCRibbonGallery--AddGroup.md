---
title: "CMFCRibbonGallery::AddGroup"
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
ms.assetid: 3f19b6bf-2b30-4576-bc87-ee0087b563b5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::AddGroup
Adds a new group to the gallery.  
  
## Syntax  
  
```  
void AddGroup(  
    LPCTSTR lpszGroupName,  
    UINT uiImagesPaletteResID,  
    int cxPaletteImage   
);  
void AddGroup(  
    LPCTSTR lpszGroupName,  
    CMFCToolBarImages& imagesGroup   
);  
void AddGroup(  
    LPCTSTR lpszGroupName,  
    int nIconsNum   
);  
```  
  
#### Parameters  
 [in] `lpszGroupName`  
 Specifies the name of the group.  
  
 [in] `uiImagesPaletteResID`  
 Specifies the resource ID of the image list that contains the images for the group.  
  
 [in] `cxPaletteImage`  
 Specifies the width in pixels of an image.  
  
 [in] `imagesGroup`  
 A reference to image list that contains group images.  
  
 [in] `nIconsNum`  
 Specifies the number of icons in the group. This parameter should be specified only for custom (owner drawn) groups.  
  
## Remarks  
 You can divide the items on a ribbon gallery into multiple groups by calling this method. Each group can have a caption.  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)