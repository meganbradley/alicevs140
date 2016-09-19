---
title: "CMFCListCtrl::RemoveSortColumn"
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
ms.assetid: a16a04b8-4746-4040-b13f-f8e2d4f39e4f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCListCtrl::RemoveSortColumn
Removes a sort column from the list of sorted columns.  
  
## Syntax  
  
```  
void RemoveSortColumn(  
   int iColumn   
);  
```  
  
#### Parameters  
 [in] `iColumn`  
 The column to remove.  
  
## Remarks  
 This method removes a sort column from the header control. It calls [CMFCHeaderCtrl::RemoveSortColumn](../vs140/CMFCHeaderCtrl--RemoveSortColumn.md).  
  
## Requirements  
 **Header:** afxlistctrl.h  
  
## See Also  
 [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)