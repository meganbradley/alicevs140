---
title: "CDockablePane::CreateTabbedPane"
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
ms.assetid: 9815e840-edce-4ccd-a27f-b7f3e88297d3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::CreateTabbedPane
Creates a tabbed pane from the current pane.  
  
## Syntax  
  
```  
virtual CTabbedPane* CreateTabbedPane();  
```  
  
## Return Value  
 The new tabbed pane, or `NULL` if the create operation failed.  
  
## Remarks  
 The framework calls this method when it creates a tabbed pane to replace this pane. For more information, see [CDockablePane::AttachToTabWnd](../vs140/CDockablePane--AttachToTabWnd.md).  
  
 Override this method in a derived class to customize how tabbed panes are created and initialized.  
  
 The tabbed pane is created according to the runtime class information stored in the `m_pTabbedControlBarRTC` member, which is initialized by the [CDockablePane::CreateEx](../vs140/CDockablePane--CreateEx.md) method.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)