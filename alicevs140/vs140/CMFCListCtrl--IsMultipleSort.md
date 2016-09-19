---
title: "CMFCListCtrl::IsMultipleSort"
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
ms.assetid: f10d8018-e919-4ff0-b53c-9325ef9af896
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCListCtrl::IsMultipleSort
Checks whether the list control currently supports sorting on multiple columns.  
  
## Syntax  
  
```  
BOOL IsMultipleSort() const;  
```  
  
## Return Value  
 `TRUE` if the list control supports multiple sort; `FALSE` otherwise.  
  
## Remarks  
 When a [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md) supports multiple sorting, the user can sort the data in the list control by multiple columns. To enable multiple sorting, call [CMFCListCtrl::EnableMultipleSort](../vs140/CMFCListCtrl--EnableMultipleSort.md).  
  
## Requirements  
 **Header:** afxlistctrl.h  
  
## See Also  
 [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCListCtrl::EnableMultipleSort](../vs140/CMFCListCtrl--EnableMultipleSort.md)