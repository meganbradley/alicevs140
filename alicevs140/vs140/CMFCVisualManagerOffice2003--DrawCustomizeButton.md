---
title: "CMFCVisualManagerOffice2003::DrawCustomizeButton"
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
ms.assetid: 22e46d9d-f5f4-42a0-a645-e4e12b5400b6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::DrawCustomizeButton
Draws a customize button.  
  
## Syntax  
  
```  
virtual void DrawCustomizeButton(  
   CDC* pDC,  
   CRect rect,  
   BOOL bIsHorz,  
   CMFCVisualManager::AFX_BUTTON_STATE state,  
   BOOL bIsCustomize,  
   BOOL bIsMoreButtons  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a display context.  
  
 [in] `rect`  
 The bounding rectangle of the button  
  
 [in] `bIsHorz`  
 `TRUE` if the button is horizontal, or `FALSE` if it is vertical.  
  
 [in] `state`  
 The state of the button as it is to be drawn (regular, pressed or highlighted).  
  
 [in] `bIsCustomize`  
 `TRUE` if the customize arrow-down or arrow-left image should be drawn in the button rectangle, or `FALSE` if not.  
  
 [in] `bIsMoreButtons`  
 `TRUE` if the horizontal or vertical customize More-Buttons image should be drawn in the button rectangle, or `FALSE` if not.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)