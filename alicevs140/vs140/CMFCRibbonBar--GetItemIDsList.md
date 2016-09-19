---
title: "CMFCRibbonBar::GetItemIDsList"
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
ms.assetid: 84b91619-6ccc-495f-a44a-1e6d59925737
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::GetItemIDsList
Retrieves the command IDs for the specified collection of ribbon elements on the ribbon bar.  
  
## Syntax  
  
```  
void GetItemIDsList(  
   CList<UINT, UINT>& lstItems,  
   BOOL bHiddenOnly = FALSE  
) const;  
```  
  
#### Parameters  
 [out] `lstItems`  
 The list of command IDs for ribbon elements that are contained in the ribbon bar.  
  
 [in] `bHiddenOnly`  
 `TRUE` to exclude ribbon elements that are displayed; `FALSE` to include all ribbon elements in the ribbon bar.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)