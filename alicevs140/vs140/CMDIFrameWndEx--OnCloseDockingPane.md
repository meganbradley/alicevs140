---
title: "CMDIFrameWndEx::OnCloseDockingPane"
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
ms.assetid: cc240c48-764d-4b71-9cd7-c0573cdacfb1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnCloseDockingPane
Called by the framework when the user clicks the **Close** button on a dockable pane.  
  
## Syntax  
  
```  
virtual BOOL OnCloseDockingPane(  
   CDockablePane* pWnd   
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 Pointer to the pane being closed.  
  
## Return Value  
 `TRUE` if the docking pane can be closed. Otherwise, `FALSE`.  
  
## Remarks  
 Override this method to handle hiding of docking panes. Return `FALSE` if you want to prevent a docking pane from being hidden.  
  
 The default implementation does nothing and returns `TRUE`.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)