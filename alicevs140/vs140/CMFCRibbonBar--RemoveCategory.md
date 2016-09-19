---
title: "CMFCRibbonBar::RemoveCategory"
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
ms.assetid: 6e979c4c-21bd-4e72-a3f4-fc286899153c
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::RemoveCategory
Deletes the specified ribbon category from the ribbon bar.  
  
## Syntax  
  
```  
BOOL RemoveCategory(  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `nIndex`  
 The zero-based index of a category in the list of ribbon categories that is contained in the ribbon bar.  
  
## Return Value  
 `TRUE` if the specified ribbon category was deleted; otherwise `FALSE`.  
  
## Remarks  
 The specified ribbon category is deleted from memory and from the category list.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)