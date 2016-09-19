---
title: "CMFCRibbonBar::DrawMenuImage"
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
ms.assetid: 5523e575-57af-4e3b-829e-c8f22cc2b0cf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::DrawMenuImage
Draws the image for a menu button.  
  
## Syntax  
  
```  
BOOL DrawMenuImage(  
   CDC* pDC,  
   const CMFCToolBarMenuButton* pMenuItem,  
   const CRect& rectImage  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context for the menu button.  
  
 [in] `pMenuItem`  
 Pointer to a toolbar menu button.  
  
 [in] `rectImage`  
 The display rectangle for a menu button.  
  
## Return Value  
 `TRUE` if the image was drawn; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)