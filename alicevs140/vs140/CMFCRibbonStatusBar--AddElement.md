---
title: "CMFCRibbonStatusBar::AddElement"
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
ms.assetid: 662cbe35-4760-4901-b003-545c727fc679
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::AddElement
Adds a new ribbon element to the ribbon status bar.  
  
## Syntax  
  
```  
void AddElement(  
   CMFCRibbonBaseElement* pElement,  
   LPCTSTR lpszLabel,  
   BOOL bIsVisible=TRUE   
);  
```  
  
#### Parameters  
 [in] `pElement`  
 A pointer to the added element.  
  
 [in] `lpszLabel`  
 A text label of the element.  
  
 [in] `bIsVisible`  
 `TRUE` if you want to add the element as visible, `FALSE` if you want to add the element as hidden.  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)