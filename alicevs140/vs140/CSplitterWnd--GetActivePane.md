---
title: "CSplitterWnd::GetActivePane"
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
ms.assetid: 7f4f3954-c6f8-4063-941c-400137889462
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::GetActivePane
Determines the active pane from the focus or active view in the frame.  
  
## Syntax  
  
```  
  
      virtual CWnd* GetActivePane(  
   int* pRow = NULL,  
   int* pCol = NULL  
);  
```  
  
#### Parameters  
 `pRow`  
 A pointer to an **int** to retrieve the row number of the active pane.  
  
 `pCol`  
 A pointer to an **int** to retrieve the column number of the active pane.  
  
## Return Value  
 Pointer to the active pane. **NULL** if no active pane exists.  
  
## Remarks  
 This member function is called by the framework to determine the active pane in a splitter window. Override to require an action by the user before getting the active pane.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::SetActivePane](../vs140/CSplitterWnd--SetActivePane.md)   
 [CFrameWnd::GetActiveView](../vs140/CFrameWnd--GetActiveView.md)   
 [CWnd::GetParentFrame](../vs140/CWnd--GetParentFrame.md)   
 [CWnd::GetFocus](../vs140/CWnd--GetFocus.md)