---
title: "CMFCToolBarImages::GrayImages"
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
ms.assetid: dcdb7e80-f490-47ea-a634-409406224ee9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::GrayImages
Grays the toolbar images to make them look disabled.  
  
## Syntax  
  
```  
BOOL GrayImages(  
   int nGrayImageLuminancePercentage   
);  
```  
  
#### Parameters  
 [in] `nGrayImageLuminancePercentage`  
 Luminance percentage.  
  
## Return Value  
 `TRUE` if images in the collection were grayed successfully; otherwise `FALSE`.  
  
## Remarks  
 This method modifies the toolbar images by averaging the red, green, and blue components of each pixel and multiplying the result by `nGrayImageLuminancePercentage` divided by 100. If `nGrayImageLuminancePercentage` is zero or negative, the default value of 130 is used instead.  
  
> [!NOTE]
>  If you want to undo the change, you must reload the images from the source. You can do this by calling [CMFCToolBarImages::Load](../vs140/CMFCToolBarImages--Load.md) or [CMFCToolBarImages::UpdateImage](../vs140/CMFCToolBarImages--UpdateImage.md) (only for user-defined images), or by calling [CMFCToolBarImages::Clear](../vs140/CMFCToolBarImages--Clear.md) and adding the images again by calling [CMFCToolBarImages::AddIcon](../vs140/CMFCToolBarImages--AddIcon.md) or [CMFCToolBarImages::AddImage](../vs140/CMFCToolBarImages--AddImage.md).  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)