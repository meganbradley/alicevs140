---
title: "CMFCRibbonBar::GetCategoryIndex"
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
ms.assetid: 4b573f4e-0b69-4ca3-915c-5f95d1ed3080
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetCategoryIndex
Retrieves the index of the specified ribbon category.  
  
## Syntax  
  
```  
int GetCategoryIndex(  
   CMFCRibbonCategory* pCategory   
) const;  
```  
  
#### Parameters  
 [in] `pCategory`  
 Pointer to a ribbon category.  
  
## Return Value  
 The zero-based index of a ribbon category specified by `pCategory`; or -1 if the ribbon category is not found.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)