---
title: "CMFCListCtrl::OnGetCellTextColor"
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
ms.assetid: 6dac351e-a9fc-4848-a73f-f0050205b0f4
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCListCtrl::OnGetCellTextColor
The framework calls this method when it must determine the text color of an individual cell.  
  
## Syntax  
  
```  
virtual COLORREF OnGetCellTextColor(  
   int nRow,  
   int nColumn   
);  
```  
  
#### Parameters  
 [in] `nRow`  
 The row of the cell in question.  
  
 [in] `nColumn`  
 The column of the cell in question.  
  
## Return Value  
 A `COLOREF` value that specifies the text color of the cell.  
  
## Remarks  
 By default, this method calls `GetTextColor` regardless of input parameters. The whole list control will have the same text color. You can override `OnGetCellTextColor` in a derived class to mark individual cells with a separate text color.  
  
## Requirements  
 **Header:** afxlistctrl.h  
  
## See Also  
 [CMFCListCtrl Class](../vs140/CMFCListCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)