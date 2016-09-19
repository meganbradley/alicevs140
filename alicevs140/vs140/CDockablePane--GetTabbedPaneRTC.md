---
title: "CDockablePane::GetTabbedPaneRTC"
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
ms.assetid: 7ce0ca86-fe62-4823-975c-04604d2f6f59
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::GetTabbedPaneRTC
Returns the runtime class information about a tabbed window that is created when another pane docks to the current pane.  
  
## Syntax  
  
```  
CRuntimeClass* GetTabbedPaneRTC() const;  
```  
  
## Return Value  
 The runtime class information for the dockable pane.  
  
## Remarks  
 Call this method to retrieve the runtime class information for tabbed panes that are created dynamically. This can occur when a user drags one pane to the caption of another pane, or if you call the [CDockablePane::AttachToTabWnd](../vs140/CDockablePane--AttachToTabWnd.md) method to programmatically create a tabbed pane from two dockable panes.  
  
 You can set the runtime class information by calling the [CDockablePane::SetTabbedPaneRTC](../vs140/CDockablePane--SetTabbedPaneRTC.md) method.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)