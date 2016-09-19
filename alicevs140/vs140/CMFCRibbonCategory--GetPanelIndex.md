---
title: "CMFCRibbonCategory::GetPanelIndex"
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
ms.assetid: eca8334f-7328-4fdc-87d9-d4cc85241752
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::GetPanelIndex
Retrieves the zero-based index of the specified ribbon panel.  
  
## Syntax  
  
```  
int GetPanelIndex(  
   const CMFCRibbonPanel* pPanel   
) const;  
```  
  
#### Parameters  
 [in] `pPanel`  
 Pointer to a ribbon panel.  
  
## Return Value  
 Zero-based index of the specified ribbon panel if the method was successful; otherwise -1.  
  
## Remarks  
 Only ribbon panels that are contained in the ribbon category are searched.  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)