---
title: "CSplitterWnd::SetColumnInfo"
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
ms.assetid: a79989fc-3a57-4b6d-839a-108c333b6a6d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::SetColumnInfo
Call to set the specified column information.  
  
## Syntax  
  
```  
  
      void SetColumnInfo(  
   int col,  
   int cxIdeal,  
   int cxMin   
);  
```  
  
#### Parameters  
 `col`  
 Specifies a splitter window column.  
  
 *cxIdeal*  
 Specifies an ideal width for the splitter window column in pixels.  
  
 `cxMin`  
 Specifies a minimum width for the splitter window column in pixels.  
  
## Remarks  
 Call this member function to set a new minimum width and ideal width for a column. The column minimum value determines when the column will be too small to be fully displayed.  
  
 When the framework displays the splitter window, it lays out the panes in columns and rows according to their ideal dimensions, working from the upper-left to the lower-right corner of the splitter window's client area.  
  
## Example  
 [!CODE [NVC_MFCWindowing#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#6)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::GetRowInfo](../vs140/CSplitterWnd--GetRowInfo.md)   
 [CSplitterWnd::RecalcLayout](../vs140/CSplitterWnd--RecalcLayout.md)