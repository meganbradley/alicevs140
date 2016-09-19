---
title: "CMFCHeaderCtrl::SetSortColumn"
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
ms.assetid: 45a48849-75a5-4f3b-8a05-99f4b5ce5480
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCHeaderCtrl::SetSortColumn
Sets the sort order of a specified column in a header control.  
  
## Syntax  
  
```  
void SetSortColumn(  
   int iColumn,  
   BOOL bAscending=TRUE,  
   BOOL bAdd=FALSE   
);  
```  
  
#### Parameters  
 [in] `iColumn`  
 The zero-based index of a header control column. If this parameter is less than zero, this method removes all columns from the list of sort columns.  
  
 [in] `bAscending`  
 Specifies the sort order of the column that the `iColumn` parameter specifies. `TRUE` to set ascending order; `FALSE` to set descending order. The default value is `TRUE`.  
  
 [in] `bAdd`  
 `TRUE` to set the sort order of the column that the `iColumn` parameter specifies.  
  
 If the current header control is in *multiple column sort* mode, this method adds the specified column to the list of sort columns. Use [CMFCHeaderCtrl::EnableMultipleSort](../vs140/CMFCHeaderCtrl--EnableMultipleSort.md) to set multiple column sort mode.  
  
 If multiple column sort mode is not set and this method is compiled in debug mode, this method asserts. If multiple column sort mode is not set and this method is compiled in retail mode, this method first removes all columns from the list of sort columns, and then adds the specified column to the list.  
  
 `FALSE` to first remove all columns from the list of sort columns, and then add the specified column to the list. The default value is `FALSE`.  
  
## Remarks  
 Use this method to set the sort order of a column. If necessary, this method adds the column to the list of sort columns. The header control uses the sort order to draw a sort arrow that points up or down.  
  
## Requirements  
 **Header:** afxheaderctrl.h  
  
## See Also  
 [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCHeaderCtrl::EnableMultipleSort](../vs140/CMFCHeaderCtrl--EnableMultipleSort.md)