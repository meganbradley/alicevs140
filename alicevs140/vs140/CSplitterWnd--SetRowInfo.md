---
title: "CSplitterWnd::SetRowInfo"
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
ms.assetid: 5a1edd20-c2dc-447b-a44e-dd7594887889
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::SetRowInfo
Call to set the specified row information.  
  
## Syntax  
  
```  
  
      void SetRowInfo(  
   int row,  
   int cyIdeal,  
   int cyMin   
);  
```  
  
#### Parameters  
 `row`  
 Specifies a splitter window row.  
  
 *cyIdeal*  
 Specifies an ideal height for the splitter window row in pixels.  
  
 `cyMin`  
 Specifies a minimum height for the splitter window row in pixels.  
  
## Remarks  
 Call this member function to set a new minimum height and ideal height for a row. The row minimum value determines when the row will be too small to be fully displayed.  
  
 When the framework displays the splitter window, it lays out the panes in columns and rows according to their ideal dimensions, working from the upper-left to the lower-right corner of the splitter window's client area.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::GetRowInfo](../vs140/CSplitterWnd--GetRowInfo.md)   
 [CSplitterWnd::SetColumnInfo](../vs140/CSplitterWnd--SetColumnInfo.md)   
 [CSplitterWnd::RecalcLayout](../vs140/CSplitterWnd--RecalcLayout.md)