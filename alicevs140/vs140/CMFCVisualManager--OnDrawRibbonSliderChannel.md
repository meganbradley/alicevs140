---
title: "CMFCVisualManager::OnDrawRibbonSliderChannel"
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
ms.assetid: 70a6405e-6cfc-4ba1-bc31-db65336da7cd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawRibbonSliderChannel
The framework calls this method when it draws the channel of a [CMFCRibbonSlider Class](../vs140/CMFCRibbonSlider-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawRibbonSliderChannel(  
   CDC* pDC,  
   CMFCRibbonSlider* pSlider,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pSlider`  
 A pointer to a CMFCRibbonSlider object. The framework draws the channel for this ribbon slider.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries for the channel of the ribbon slider.  
  
## Remarks  
 Override this method in a derived class to customize the appearance of the channel of the ribbon slider.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonSlider Class](../vs140/CMFCRibbonSlider-Class.md)