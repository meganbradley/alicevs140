---
title: "CDockablePane::IsHideInAutoHideMode"
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
ms.assetid: 25d4ccaa-8b82-4aac-ad64-7fc4e6ccaa3a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::IsHideInAutoHideMode
Determines the behavior of a pane that is in autohide mode if it is shown (or hidden) by calling [CDockablePane::ShowPane](../vs140/CDockablePane--ShowPane.md).  
  
## Syntax  
  
```  
virtual BOOL IsHideInAutoHideMode() const;  
```  
  
## Return Value  
 `TRUE` if the dockable pane should be hidden when in autohide mode; otherwise, `FALSE`.  
  
## Remarks  
 When a dockable pane is in autohide mode, it behaves differently when you call `ShowPane` to hide or show the pane. This behavior is controlled by the static member [CDockablePane::m_bHideInAutoHideMode](../vs140/CDockablePane--m_bHideInAutoHideMode.md). If this member is `TRUE`, the dockable pane and its related autohide toolbar or autohide button is hidden or shown when you call `ShowPane`. Otherwise, the dockable pane is activated or deactivated, and its related autohide toolbar or autohide button is always visible.  
  
 Override this method in a derived class to change the default behavior for individual panes.  
  
 The default value for `m_bHideInAutoHideMode` is `FALSE`.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCAutoHideBar Class](../vs140/CMFCAutoHideBar-Class.md)   
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)