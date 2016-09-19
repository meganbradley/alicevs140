---
title: "CMFCRibbonStatusBar::AddExtendedElement"
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
ms.assetid: d5192289-0d87-462e-a7e0-c936decb6e27
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::AddExtendedElement
Adds a ribbon element to the extended area of the ribbon status bar.  
  
## Syntax  
  
```  
void AddExtendedElement(  
   CMFCRibbonBaseElement* pElement,  
   LPCTSTR lpszLabel,  
   BOOL bIsVisible=TRUE   
);  
```  
  
#### Parameters  
 [in] `pElement`  
 A pointer to the added element.  
  
 [in] `lpszLabel`  
 The text label of the element.  
  
 [in] `bIsVisible`  
 `TRUE` if you want to add the element as visible, `FALSE` if you want to add the element as hidden.  
  
## Remarks  
 The extended area is on the right side of the status bar control.  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)