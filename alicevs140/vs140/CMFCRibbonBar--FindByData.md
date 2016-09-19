---
title: "CMFCRibbonBar::FindByData"
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
ms.assetid: 98bede59-041c-435d-bc74-07d68ac98bff
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::FindByData
Retrieves a pointer to a ribbon element if it has the specified data and visibility.  
  
## Syntax  
  
```  
CMFCRibbonBaseElement* FindByData(  
   DWORD_PTR dwData,  
   BOOL bVisibleOnly = TRUE   
) const;  
```  
  
#### Parameters  
 [in] `dwData`  
 The data associated with a ribbon element.  
  
 [in] `bVisibleOnly`  
 `TRUE` to search visible ribbon elements only; `FALSE` to search all ribbon elements.  
  
## Return Value  
 A pointer to a ribbon element if it has the specified data and visibility; otherwise `NULL`.  
  
## Remarks  
 A ribbon element is any control that you can add to the ribbon, such as a ribbon button, or a ribbon category, or a ribbon slider.  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)