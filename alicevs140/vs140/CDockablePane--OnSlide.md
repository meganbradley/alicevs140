---
title: "CDockablePane::OnSlide"
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
ms.assetid: 921cc771-6259-4a03-a4b4-4778b0b7b750
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::OnSlide
Called by the framework to animate the pane when it is in autohide mode.  
  
## Syntax  
  
```  
virtual void OnSlide(  
    BOOL bSlideOut  
);  
```  
  
#### Parameters  
 [in] `bSlideOut`  
 `TRUE` to show the pane; `FALSE` to hide the pane.  
  
## Remarks  
 Override this method in a derived class to implement custom autohide effects.  
  
## Requirements  
 **Header:** afxDockablePane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)