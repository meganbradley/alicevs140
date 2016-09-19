---
title: "CMFCRibbonStatusBar::AddDynamicElement"
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
ms.assetid: 9aa4d22b-3d01-4086-a674-18f2e088e312
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::AddDynamicElement
Adds a dynamic element to the ribbon status bar.  
  
## Syntax  
  
```  
void AddDynamicElement(  
   CMFCRibbonBaseElement* pElement   
);  
```  
  
#### Parameters  
 [in] `pElement`  
 A pointer to a dynamic element.  
  
## Remarks  
 Unlike regular elements, dynamic elements are not customizable and the customize menu of the status bar does not display them.  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)