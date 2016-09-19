---
title: "CMFCRibbonBar::HideAllContextCategories"
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
ms.assetid: 0948d971-0799-481f-b29f-aa9b1b983d95
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::HideAllContextCategories
Hides all the context categories on the ribbon bar.  
  
## Syntax  
  
```  
BOOL HideAllContextCategories();  
```  
  
## Return Value  
 `TRUE` if at least one context category was hidden; otherwise, `FALSE`.  
  
## Remarks  
 If a context category is active, the active category is reset to the first visible category in the category list.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)