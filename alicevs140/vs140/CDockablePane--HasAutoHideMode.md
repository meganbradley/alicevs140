---
title: "CDockablePane::HasAutoHideMode"
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
ms.assetid: 02a5c468-5c7c-4f3f-824c-5ecef1fb2d9e
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::HasAutoHideMode
Specifies whether a docking pane can be switched to autohide mode.  
  
## Syntax  
  
```  
virtual BOOL HasAutoHideMode() const;  
```  
  
## Return Value  
 `TRUE` if the dockable pane can be switched to autohide mode; otherwise, `FALSE`.  
  
## Remarks  
 Override this method in a derived class to disable autohide mode for a specific dockable pane.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)