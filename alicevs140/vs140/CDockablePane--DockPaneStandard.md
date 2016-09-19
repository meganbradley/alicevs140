---
title: "CDockablePane::DockPaneStandard"
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
ms.assetid: 3a1e3b19-f2a1-4f26-be07-799a3c69002a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::DockPaneStandard
Docks a pane by using outline (standard) docking.  
  
## Syntax  
  
```  
virtual CPane* DockPaneStandard(  
   BOOL& bWasDocked  
);  
```  
  
#### Parameters  
 [in] `bWasDocked`  
 When the method returns, this value contains `TRUE` if the pane was successfully docked; otherwise, it contains `FALSE`.  
  
## Return Value  
 If the pane was docked to a tabbed window, or if a tabbed window was created as a result of docking, this method returns a pointer to the tabbed window. If the pane was otherwise successfully docked, this method returns the `this` pointer. If docking failed, this method returns `NULL`.  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)