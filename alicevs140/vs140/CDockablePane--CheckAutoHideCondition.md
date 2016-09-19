---
title: "CDockablePane::CheckAutoHideCondition"
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
ms.assetid: 0e332d83-232e-4c14-8ed8-91b6585af83d
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::CheckAutoHideCondition
Determines whether the docking pane is hidden (also known as autohide mode).  
  
## Syntax  
  
```  
virtual BOOL CheckAutoHideCondition();  
```  
  
## Return Value  
 `TRUE` if the hide condition is met; otherwise, `FALSE`.  
  
## Remarks  
 The framework uses a timer to periodically check whether to hide an autohide dockable pane. The method returns `TRUE` when the pane is not active, the pane is not being resized, and the mouse pointer is not over the pane.  
  
 If all the previous conditions are met, the framework calls [CDockablePane::Slide](../vs140/CDockablePane--Slide.md) to hide the pane.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)