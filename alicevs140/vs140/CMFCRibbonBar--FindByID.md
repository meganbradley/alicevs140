---
title: "CMFCRibbonBar::FindByID"
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
ms.assetid: dde66b4b-22d8-452e-bf15-b63ebe503b5e
caps.latest.revision: 22
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::FindByID
Retrieves a pointer to the ribbon element that has the specified command ID and search values.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* FindByID(  
   UINT uiCmdID,  
   BOOL bVisibleOnly = TRUE,  
   BOOL bExcludeQAT = FALSE   
) const;  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 Command ID for a ribbon element.  
  
 [in] `bVisibleOnly`  
 `TRUE` to search visible ribbon elements only; `FALSE` to search all ribbon elements.  
  
 [in] `bExcludeQAT`  
 `TRUE` to exclude quick access toolbar elements from the search; otherwise, `FALSE`.  
  
## Return Value  
 A pointer to a ribbon element if it has the specified command ID and search values; otherwise, `NULL`.  
  
## Remarks  
 A ribbon element is any ribbon control that can be added to the ribbon, such as a ribbon button, or a ribbon category, or a ribbon slider.  
  
 In general, there can be more than one ribbon element that has the same command ID. If you want to obtain pointers to all ribbon elements that use a specified command ID, use the [CMFCRibbonBar::GetElementsByID](../vs140/CMFCRibbonBar--GetElementsByID.md) method.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)