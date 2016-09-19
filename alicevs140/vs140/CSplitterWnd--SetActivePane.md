---
title: "CSplitterWnd::SetActivePane"
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
ms.assetid: 70697a82-8d57-4612-a5bd-6267a2c9da15
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSplitterWnd::SetActivePane
Sets a pane to be the active one in the frame.  
  
## Syntax  
  
```  
  
      virtual void SetActivePane(  
   int row,  
   int col,  
   CWnd* pWnd = NULL   
);  
```  
  
#### Parameters  
 `row`  
 If `pWnd` is **NULL**, specifies the row in the pane that will be active.  
  
 `col`  
 If `pWnd` is **NULL**, specifies the column in the pane that will be active.  
  
 `pWnd`  
 A pointer to a `CWnd` object. If **NULL**, the pane specified by `row` and `col` is set active. If not **NULL**, specifies the pane that is set active.  
  
## Remarks  
 This member function is called by the framework to set a pane as active when the user changes the focus to a pane within the frame window. You can explicitly call `SetActivePane` to change the focus to the specified view.  
  
 Specify pane by providing either row and column, **or** by providing `pWnd`.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CSplitterWnd Class](../vs140/CSplitterWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWnd::GetActivePane](../vs140/CSplitterWnd--GetActivePane.md)   
 [CSplitterWnd::GetPane](../vs140/CSplitterWnd--GetPane.md)   
 [CFrameWnd::SetActiveView](../vs140/CFrameWnd--SetActiveView.md)