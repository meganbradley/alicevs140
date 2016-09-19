---
title: "CMFCListCtrl::Sort"
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
ms.assetid: 1077dd81-9945-43cf-bb8f-c6278195d649
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCListCtrl::Sort
Sorts the list control.  
  
## Syntax  
  
```  
virtual void Sort(  
   int iColumn,  
   BOOL bAscending = TRUE,  
   BOOL bAdd = FALSE   
);  
```  
  
#### Parameters  
 [in] `iColumn`  
 The column to sort.  
  
 [in] `bAscending`  
 A Boolean that specifies the sort order.  
  
 [in] `bAdd`  
 A Boolean that specifies whether this method adds the column indicated by `iColumn` to the list of sort columns.  
  
## Requirements  
 **Header:** afxlistctrl.h  
  
## See Also  
 [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)