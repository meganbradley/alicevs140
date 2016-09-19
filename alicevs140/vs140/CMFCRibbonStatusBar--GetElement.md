---
title: "CMFCRibbonStatusBar::GetElement"
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
ms.assetid: 1f62ff7b-22ec-427a-bd18-7d17158d1d89
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBar::GetElement
Returns a pointer to the element that is located at a specified index.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* GetElement(  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies a zero-based index of an element that is located in the main area of the status bar control.  
  
## Return Value  
 A pointer to the element that is located at the specified index. `NULL` if the index is negative or exceeds the number of elements in the status bar.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonstatusbar.h  
  
## See Also  
 [CMFCRibbonStatusBar Class](../vs140/CMFCRibbonStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)