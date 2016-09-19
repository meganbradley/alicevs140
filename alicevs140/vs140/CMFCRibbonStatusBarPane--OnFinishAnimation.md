---
title: "CMFCRibbonStatusBarPane::OnFinishAnimation"
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
ms.assetid: 2cd51372-c705-4504-82f7-0ad8eb582c2f
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonStatusBarPane::OnFinishAnimation
Framework calls this method when the animation that is assigned to the pane ends.  
  
## Syntax  
  
```  
virtual void OnFinishAnimation();  
```  
  
## Remarks  
 `StopAnimation` method calls the `OnFinishAnimation` method, which you can use to clean up data when the animation ends.  
  
## Requirements  
 **Header:** afxribbonstatusbarpane.h  
  
## See Also  
 [CMFCRibbonStatusBarPane Class](../vs140/CMFCRibbonStatusBarPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)