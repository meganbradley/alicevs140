---
title: "CMFCHeaderCtrl::GetColumnState"
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
ms.assetid: 1369045f-49ce-4e31-a97b-1928189a3058
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCHeaderCtrl::GetColumnState
Indicates whether a column is unsorted, or is sorted in ascending or descending order.  
  
## Syntax  
  
```  
int GetColumnState(  
   int iColumn   
) const;  
```  
  
#### Parameters  
 [in] `iColumn`  
 The zero-based index of a column.  
  
## Return Value  
 A value that indicate the sort status of the specified column. The following table lists the possible values:  
  
|Value|Description|  
|-----------|-----------------|  
|-1|Sorted in descending order.|  
|0|Not sorted.|  
|1|Sorted in ascending order.|  
  
## Remarks  
  
## Requirements  
 **Header:** afxheaderctrl.h  
  
## See Also  
 [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)