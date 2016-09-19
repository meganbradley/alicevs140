---
title: "CMFCRibbonCategory::FindByData"
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
ms.assetid: b83c8a86-1955-4d22-994f-0dde29bf62d2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::FindByData
Retrieves the ribbon element associated with the specified data.  
  
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
 `TRUE` to include quick access ribbon elements in the search; `FALSE` to exclude quick access ribbon elements in the search.  
  
## Return Value  
 Pointer to a ribbon element if the method was successful; otherwise `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)