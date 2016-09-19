---
title: "CMFCRibbonBar::ShowContextCategories"
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
ms.assetid: 8d5f0dcb-6740-45cd-b171-11acae2b17c3
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::ShowContextCategories
Shows or hides the context categories that have the specified ID.  
  
## Syntax  
  
```  
void ShowContextCategories(  
   UINT uiContextID,  
   BOOL bShow=TRUE   
);  
```  
  
#### Parameters  
 [in] `uiContextID`  
 The context category ID.  
  
 [in] `bShow`  
 If `TRUE`, show the categories that have the specified ID; otherwise, hide the categories that have the specified ID.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)