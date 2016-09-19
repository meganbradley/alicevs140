---
title: "CSplitterWnd::GetPane"
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
ms.assetid: bebcaeec-3560-44cf-80eb-ed84eb027da7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::GetPane
Returns the pane at the specified row and column.  
  
## Syntax  
  
```  
  
      CWnd* GetPane(  
   int row,  
   int col   
) const;  
```  
  
#### Parameters  
 `row`  
 Specifies a row.  
  
 `col`  
 Specifies a column.  
  
## Return Value  
 Returns the pane at the specified row and column. The returned pane is usually a [CView](../vs140/CView-Class.md)-derived class.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::GetActivePane](../vs140/CSplitterWnd--GetActivePane.md)   
 [CSplitterWnd::IdFromRowCol](../vs140/CSplitterWnd--IdFromRowCol.md)   
 [CSplitterWnd::IsChildPane](../vs140/CSplitterWnd--IsChildPane.md)