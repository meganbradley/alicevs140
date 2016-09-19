---
title: "CMFCRibbonGallery::EnableMenuResize"
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
ms.assetid: 01649d69-6f66-4df0-be82-2c400de8ceb4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonGallery::EnableMenuResize
Enables or disables resizing of the menu panel.  
  
## Syntax  
  
```  
void EnableMenuResize(  
    BOOL bEnable = TRUE,  
    BOOL bVertcalOnly = FALSE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable resizing the menu; otherwise, `FALSE`.  
  
 [in] `bVertcalOnly`  
 `TRUE` to specify that the gallery can be resized only vertically; `FALSE` to specify that the gallery can be resized both vertically and horizontally.  
  
## Remarks  
 Use this method to enable or disable resizing the ribbon gallery. When resizing is enabled, the ribbon gallery displays a gripper that a user can use to resize it.  
  
## Requirements  
 **Header:** afxRibbonPaletteGallery.h  
  
## See Also  
 [CMFCRibbonGallery Class](../vs140/CMFCRibbonGallery-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)