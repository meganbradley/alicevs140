---
title: "CDockablePane::CanBeAttached"
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
ms.assetid: 0aa4d1ca-a25e-4a97-87c8-ec8ca7ae6102
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::CanBeAttached
Determines whether the current pane can be docked to another pane.  
  
## Syntax  
  
```  
virtual BOOL CanBeAttached() const;  
```  
  
## Return Value  
 `TRUE` if the dockable pane can be docked to another pane or to the main frame window; otherwise, `FALSE`.  
  
## Remarks  
 By default, this method always returns `TRUE`. Override this method in a derived class to enable or disable docking without calling [CBasePane::EnableDocking](../vs140/CBasePane--EnableDocking.md).  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)