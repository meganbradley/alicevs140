---
title: "CMFCToolBar::AutoGrayInactiveImages"
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
ms.assetid: 6ef05d1d-2dc1-48d9-bf15-2ebe92477952
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::AutoGrayInactiveImages
Enable or disables the automatic generation of inactive button images.  
  
## Syntax  
  
```  
static void AutoGrayInactiveImages(  
   BOOL bEnable=TRUE,  
   int nGrayImagePercentage=0,  
   BOOL bRedrawAllToolbars=TRUE   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 A Boolean value that specifies whether to dim inactive images. If this parameter is `TRUE`, inactive images are dimmed. Otherwise, inactive images are not dimmed.  
  
 [in] `nGrayImagePercentage`  
 Specifies the luminance percentage for inactive images. If `bEnable` is `FALSE`, this value is ignored.  
  
 [in] `bRedrawAllToolbars`  
 A Boolean value that specifies whether to redraw all toolbars in the application. If this parameter is `TRUE`, this method redraws all toolbars.  
  
## Remarks  
 If `bEnable` is `TRUE`, the framework uses `nGrayImagePercentage` to generate inactive images from the regular images. Otherwise, you must provide the set of inactive images by using the [CMFCToolBar::GetColdImages](../vs140/CMFCToolBar--GetColdImages.md) method. By default, this option is disabled.  
  
 For more information about the `nGrayImagePercentage` parameter, see [CMFCToolBarImages::GrayImages](../vs140/CMFCToolBarImages--GrayImages.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetColdImages](../vs140/CMFCToolBar--GetColdImages.md)   
 [CMFCToolBarImages::GrayImages](../vs140/CMFCToolBarImages--GrayImages.md)