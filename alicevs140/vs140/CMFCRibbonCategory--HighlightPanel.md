---
title: "CMFCRibbonCategory::HighlightPanel"
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
ms.assetid: c75a2414-84c7-4acd-bc0d-867d4508b7cd
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::HighlightPanel
Highlights the specified ribbon panel.  
  
## Syntax  
  
```  
CMFCRibbonPanel* HighlightPanel(  
   CMFCRibbonPanel* pHLPanel,  
   CPoint point  
);  
```  
  
#### Parameters  
 [in] `pHLPanel`  
 Pointer to the ribbon panel to highlight.  
  
 [in] `point`  
 The x and y coordinates of the pointer, relative to the upper-left corner of the window.  
  
## Return Value  
 Pointer to the previously highlighted ribbon panel; otherwise `NULL` if no ribbon panel is highlighted when this method is invoked.  
  
## Remarks  
 For more information about highlighting a ribbon panel, see [CMFCRibbonPanel::Highlight](../vs140/CMFCRibbonPanel--Highlight.md).  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)