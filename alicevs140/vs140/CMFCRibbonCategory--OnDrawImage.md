---
title: "CMFCRibbonCategory::OnDrawImage"
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
ms.assetid: 8fc7a779-c42d-403c-8b24-83d265c4e3b7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::OnDrawImage
Called by the framework to draw the specified image on the ribbon category.  
  
## Syntax  
  
```  
virtual BOOL OnDrawImage(  
   CDC* pDC,  
   CRect rect,  
   CMFCRibbonBaseElement* pElement,  
   BOOL bIsLargeImage,  
   BOOL nImageIndex,  
   BOOL bCenter  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context for the image.  
  
 [in] `rect`  
 Display rectangle for the image.  
  
 [in] `pElement`  
 Pointer to the ribbon element that contains the image.  
  
 [in] `bIsLargeImage`  
 `TRUE` if the image is the large size; `FALSE` if the image is the small size.  
  
 [in] `nImageIndex`  
 Zero-based index of the image in the image array that is contained in the ribbon category.  
  
 [in] `bCenter`  
 `TRUE` to center the image in the display rectangle; `FALSE` to draw the image in the upper-left corner of the display rectangle.  
  
## Return Value  
 `TRUE` if the method was successful; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)