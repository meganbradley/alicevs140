---
title: "CListCtrl::SetColumn"
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
ms.assetid: 72e568e4-6161-4cf2-a763-f2798ad51d17
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::SetColumn
Sets the attributes of a list view column.  
  
## Syntax  
  
```  
  
      BOOL SetColumn(  
   int nCol,  
   const LVCOLUMN* pColumn   
);  
```  
  
#### Parameters  
 `nCol`  
 Index of the column whose attributes are to be set.  
  
 `pColumn`  
 Address of an [LVCOLUMN](http://msdn.microsoft.com/library/windows/desktop/bb774743) structure that contains the new column attributes, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. The structure's **mask** member specifies which column attributes to set. If the **mask** member specifies the `LVCF_TEXT` value, the structure's **pszText** member is the address of a null-terminated string and the structure's **cchTextMax** member is ignored.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 See the example for [CListCtrl::GetColumn](../vs140/CListCtrl--GetColumn.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetColumn](../vs140/CListCtrl--GetColumn.md)