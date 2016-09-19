---
title: "CMFCRibbonBar::ActivateContextCategory"
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
ms.assetid: 2827724b-5bcc-466d-9577-5c6c3545a92c
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::ActivateContextCategory
Activates a context category that is already visible.  
  
## Syntax  
  
```  
BOOL ActivateContextCategory(  
   UINT uiContextID   
);  
```  
  
#### Parameters  
 [in] `uiContextID`  
 The context category ID.  
  
## Return Value  
 `TRUE` if a context category with `uiContextID` is found and activated; otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)