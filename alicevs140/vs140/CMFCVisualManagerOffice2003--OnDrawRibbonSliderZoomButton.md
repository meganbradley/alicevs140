---
title: "CMFCVisualManagerOffice2003::OnDrawRibbonSliderZoomButton"
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
ms.assetid: 60562083-0b4b-44a4-81b1-a49b482f698a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawRibbonSliderZoomButton
The framework calls this method when it draws the zoom buttons for a [CMFCRibbonSlider](../vs140/CMFCRibbonSlider-Class.md) object.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonSliderZoomButton(  
   CDC* pDC,  
   CMFCRibbonSlider* pSlider,  
   CRect rect,  
   BOOL bIsZoomOut,  
   BOOL bIsHighlighted,  
   BOOL bIsPressed,  
   BOOL bIsDisabled  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pSlider`  
 A pointer to a [CMFCRibbonSlider](../vs140/CMFCRibbonSlider-Class.md) object. The framework draws this ribbon slider.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the zoom buttons on the ribbon slider.  
  
 [in] `bIsZoomOut`  
 `TRUE` if the framework should draw the left button with a "**-**" for zoom out, or `FALSE` if the framework should draw the right button with a "**+**" for zoom in.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the button is highlighted.  
  
 [in] `bIsPressed`  
 A Boolean parameter that indicates whether the button is pressed.  
  
 [in] `bIsDisabled`  
 A Boolean parameter that indicates whether the button is unavailable.  
  
## Remarks  
 By default, the zoom buttons on the ribbon slider are a circle with either a **+** or **-** sign in the center. To customize the appearance of zoom buttons, override this method in a derived visual manager.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)