---
title: "CDockablePane::IsVisible"
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
ms.assetid: 55e838e9-7780-47c8-aca2-9030fbc21be5
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::IsVisible
Determines whether the current pane is visible.  
  
## Syntax  
  
```  
virtual BOOL IsVisible() const;  
```  
  
## Return Value  
 `TRUE` if the dockable pane is visible; otherwise, `FALSE`.  
  
## Remarks  
 Call this method to determine whether a dockable pane is visible. You can use this method instead of calling [CWnd::IsWindowVisible](../vs140/CWnd--IsWindowVisible.md) or testing for the `WS_VISIBLE` style. The returned visibility state depends on whether autohide mode is enabled or disabled and on the value of the [CDockablePane::IsHideInAutoHideMode](../vs140/CDockablePane--IsHideInAutoHideMode.md) property.  
  
 If the dockable pane is in autohide mode and `IsHideInAutoHideMode` returns `FALSE` the visibility state is always `FALSE`.  
  
 If the dockable pane is in autohide mode and `IsHideInAutoHideMode` returns `TRUE` the visibility state depends on the visibility state of the related autohide toolbar.  
  
 If the dockable pane is not in autohide mode, the visibility state is determined by the [CBasePane::IsVisible](../vs140/CBasePane--IsVisible.md) method.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCAutoHideBar Class](../vs140/CMFCAutoHideBar-Class.md)