---
title: "CSplitterWnd::GetColumnInfo"
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
ms.assetid: bdb86dc3-1b8e-465d-b345-cd3dd61d4385
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::GetColumnInfo
Returns information on the specified column.  
  
## Syntax  
  
```  
  
      void GetColumnInfo(  
   int col,  
   int& cxCur,  
   int& cxMin   
) const;  
```  
  
#### Parameters  
 `col`  
 Specifies a column.  
  
 *cxCur*  
 A reference to an `int` to be set to the current width of the column.  
  
 `cxMin`  
 A reference to an `int` to be set to the current minimum width of the column.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::SetColumnInfo](../vs140/CSplitterWnd--SetColumnInfo.md)   
 [CSplitterWnd::GetRowInfo](../vs140/CSplitterWnd--GetRowInfo.md)