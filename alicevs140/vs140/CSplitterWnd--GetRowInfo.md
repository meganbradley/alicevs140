---
title: "CSplitterWnd::GetRowInfo"
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
ms.assetid: a08ef0c8-e921-4c80-9a8c-720ea1ad3e3e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::GetRowInfo
Returns information on the specified row.  
  
## Syntax  
  
```  
  
      void GetRowInfo(  
   int row,  
   int& cyCur,  
   int& cyMin   
) const;  
```  
  
#### Parameters  
 `row`  
 Specifies a row.  
  
 `cyCur`  
 Reference to `int` to be set to the current height of the row in pixels.  
  
 `cyMin`  
 Reference to `int` to be set to the current minimum height of the row in pixels.  
  
## Remarks  
 Call this member function to obtain information about the specified row. The `cyCur` parameter is filled with the current height of the specified row, and `cyMin` is filled with the minimum height of the row.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::SetRowInfo](../vs140/CSplitterWnd--SetRowInfo.md)   
 [CSplitterWnd::GetColumnInfo](../vs140/CSplitterWnd--GetColumnInfo.md)