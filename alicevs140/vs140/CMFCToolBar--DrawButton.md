---
title: "CMFCToolBar::DrawButton"
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
ms.assetid: 737d0e63-377c-453c-b494-097919e109ea
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::DrawButton
Repaints a toolbar button.  
  
## Syntax  
  
```  
virtual BOOL DrawButton(  
   CDC* pDC,  
   CMFCToolBarButton* pButton,  
   CMFCToolBarImages* pImages,  
   BOOL bHighlighted,  
   BOOL bDrawDisabledImages   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pButton`  
 A pointer to a button to draw.  
  
 [in] `pImages`  
 A pointer to the toolbar images.  
  
 [in] `bHighlighted`  
 `TRUE` if the button is highlighted; otherwise `FALSE`.  
  
 [in] `bDrawDisabledImages`  
 `TRUE` if disabled buttons are dimmed; otherwise `FALSE`.  
  
## Return Value  
 `TRUE` if the button was repainted; `FALSE` if the button is hidden.  
  
## Remarks  
 The [CMFCToolBar::DrawButton](../vs140/CMFCToolBar--DrawButton.md) method calls this method when a toolbar button must be repainted.  
  
 Override this method if you want to customize the appearance of buttons on your toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::DrawButton](../vs140/CMFCToolBar--DrawButton.md)