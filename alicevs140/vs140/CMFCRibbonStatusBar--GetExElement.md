---
title: "CMFCRibbonStatusBar::GetExElement"
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
ms.assetid: 6761870c-c93d-4dfb-8f75-078f9d4a5b74
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::GetExElement
Returns a pointer to the element that is located at a specified index in the extended area of the ribbon status bar. The extended area is on the right side of the status bar control.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* GetExElement(  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the zero-based index of an element that is located in the extended area of the status bar control.  
  
## Return Value  
 A pointer to the element that is located at a specified index in the extended area of the ribbon status bar. `NULL` if `nIndex` is negative or exceeds the number of elements in the extended area of the ribbon status bar.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)