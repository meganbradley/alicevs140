---
title: "CMDIFrameWndEx::OnShowPanes"
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
ms.assetid: a6962760-374d-4c30-95f1-56feadeb8bc7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnShowPanes
Called by the framework to show or hide panes.  
  
## Syntax  
  
```  
virtual BOOL OnShowPanes(  
   BOOL bShow   
);  
```  
  
#### Parameters  
 [in] `bShow`  
 `TRUE` to show panes, `FALSE` to hide panes.  
  
## Return Value  
 `TRUE` if the state of the panes changes as a result of calling this method, `FALSE` if the panes are already in the state specified by `bShow`. For example, if the panes are hidden and `bShow` is `FALSE`, the return value is `FALSE`.  
  
## Remarks  
 The default implementation removes the toolbar from the top-level frame window.  
  
 If [CDockingManager::m_bHideDockingBarsInContainerMode](../vs140/CDockingManager--m_bHideDockingBarsInContainerMode.md) is `TRUE` (the default), all docking panes will be hidden.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)