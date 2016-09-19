---
title: "CMFCRibbonCategory::HitTestScrollButtons"
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
ms.assetid: 9be71479-6f16-41b3-84ca-cbe9a161c834
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::HitTestScrollButtons
If a point falls within a ribbon category’s left or right scroll button, returns a pointer to that button.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* HitTestScrollButtons(  
   CPoint point  
) const;  
```  
  
#### Parameters  
 [in] `point`  
 The point to test.  
  
## Return Value  
 If `point` falls within the bounding rectangle of either the left or the right scroll button of the ribbon category, returns a pointer to that button, or otherwise, returns `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)