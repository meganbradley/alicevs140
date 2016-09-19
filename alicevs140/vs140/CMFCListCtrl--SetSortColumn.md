---
title: "CMFCListCtrl::SetSortColumn"
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
ms.assetid: 9984bf7c-2185-4abe-ab0e-b3700a35ddd6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCListCtrl::SetSortColumn
Sets the current sorted column and the sort order.  
  
## Syntax  
  
```  
void SetSortColumn(  
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
 A Boolean that specifies whether the method adds the column indicated by `iColumn` to the list of sort columns.  
  
## Remarks  
 This method passes the input parameters to the header control by using the method [CMFCHeaderCtrl::SetSortColumn](../vs140/CMFCHeaderCtrl--SetSortColumn.md).  
  
## Requirements  
 **Header:** afxlistctrl.h  
  
## See Also  
 [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)