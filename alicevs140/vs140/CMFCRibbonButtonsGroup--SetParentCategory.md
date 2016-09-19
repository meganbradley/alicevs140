---
title: "CMFCRibbonButtonsGroup::SetParentCategory"
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
ms.assetid: c248e708-1952-438e-9046-cd16b7130f48
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButtonsGroup::SetParentCategory
Sets the parent `CMFCRibbonCategory` of the `CMFCRibbonButtonsGroup` object and all the buttons within it.  
  
## Syntax  
  
```  
virtual void SetParentCategory(  
   CMFCRibbonCategory* pCategory  
);  
```  
  
#### Parameters  
 [in] `pCategory`  
 Pointer to the parent category to set (the tabbed groups in ribbon controls are called categories).  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbuttonsgroup.h  
  
## See Also  
 [CMFCRibbonButtonsGroup Class](../vs140/CMFCRibbonButtonsGroup-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)