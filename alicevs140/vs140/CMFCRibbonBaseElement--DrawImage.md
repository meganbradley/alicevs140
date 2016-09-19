---
title: "CMFCRibbonBaseElement::DrawImage"
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
ms.assetid: 8a9ef460-397c-4ac4-a913-69ae872efdd5
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::DrawImage
Draws the image for the ribbon element.  
  
## Syntax  
  
```  
virtual void DrawImage(  
    CDC* pDC,  
    RibbonImageType type,  
    CRect rectImage  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context.  
  
 [in] `type`  
 An image type enumerated value. See the Remarks section for a list of possible values.  
  
 [in] `rectImage`  
 The image rectangle.  
  
## Remarks  
 By default this method does nothing. Override this method in a derived class to draw the image for the ribbon element.  
  
 The following table lists possible values for the `type` parameter:  
  
 `RibbonImageLarge`  
 Large 32x32 pixel image size.  
  
 `RibbonImageSmall`  
 Small 16x16 pixel image size.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)