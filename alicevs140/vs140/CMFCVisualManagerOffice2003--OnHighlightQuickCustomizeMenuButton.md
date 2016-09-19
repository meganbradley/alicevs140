---
title: "CMFCVisualManagerOffice2003::OnHighlightQuickCustomizeMenuButton"
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
ms.assetid: 01a09259-2d5e-47f7-be05-8cc3117989e3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnHighlightQuickCustomizeMenuButton
The framework calls this method when it draws a highlighted quick-customize menu button.  
  
## Syntax  
  
```  
virtual void OnHighlightQuickCustomizeMenuButton(  
   CDC* pDC,  
   CMFCToolBarMenuButton* pButton,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context for the button.  
  
 [in] `pButton`  
 A pointer to the button.  
  
 [in] `rect`  
 The bounding rectangle of the button.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)