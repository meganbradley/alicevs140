---
title: "CDockablePane::CheckStopSlideCondition"
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
ms.assetid: 8bfb36d0-b7a3-4dc0-89c3-9a3ba07c9632
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::CheckStopSlideCondition
Determines when an autohide docking pane should stop sliding.  
  
## Syntax  
  
```  
virtual BOOL CheckStopSlideCondition(  
    BOOL bDirection   
);  
```  
  
#### Parameters  
 [in] `bDirection`  
 `TRUE` if the pane is visible; `FALSE` if the pane is hidden.  
  
## Return Value  
 `TRUE` if the stop condition is met; otherwise, `FALSE`.  
  
## Remarks  
 When a dockable pane is set to autohide mode, the framework uses sliding effects to show or hide the pane. The framework calls this function when the pane is sliding. `CheckStopSlideCondition` returns `TRUE` when the pane is fully visible or when it is fully hidden.  
  
 Override this method in a derived class to implement custom autohide effects.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockablePane::OnSlide](../vs140/CDockablePane--OnSlide.md)   
 [CDockablePane::Slide](../vs140/CDockablePane--Slide.md)