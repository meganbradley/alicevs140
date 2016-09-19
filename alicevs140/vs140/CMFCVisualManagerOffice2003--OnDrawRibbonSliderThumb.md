---
title: "CMFCVisualManagerOffice2003::OnDrawRibbonSliderThumb"
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
ms.assetid: f2bae237-ac4c-4a00-bb29-94aa9a6d6c69
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawRibbonSliderThumb
The framework calls this method when it draws the thumb of a [CMFCRibbonSlider](../vs140/CMFCRibbonSlider-Class.md) object  
  
## Syntax  
  
```  
virtual void OnDrawRibbonSliderThumb(  
   CDC* pDC,  
   CMFCRibbonSlider* pSlider,  
   CRect rect,  
   BOOL bIsHighlighted,  
   BOOL bIsPressed,  
   BOOL bIsDisabled  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pSlider`  
 A pointer to a [CMFCRibbonSlider](../vs140/CMFCRibbonSlider-Class.md). The framework draws the thumb for this ribbon slider.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the thumb for the ribbon slider.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the thumb is highlighted.  
  
 [in] `bIsPressed`  
 A Boolean parameter that indicates whether the thumb is pressed.  
  
 [in] `bIsDisabled`  
 A Boolean parameter that indicates whether the thumb is unavailable.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the thumb for a ribbon slider.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)