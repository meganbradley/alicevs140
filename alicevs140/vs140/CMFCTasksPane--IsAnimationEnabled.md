---
title: "CMFCTasksPane::IsAnimationEnabled"
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
ms.assetid: 842dfb4f-2aa8-4aa9-8ffb-94c72ad1a7d2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::IsAnimationEnabled
Indicates whether animation is enabled.  
  
## Syntax  
  
```  
BOOL IsAnimationEnabled() const;  
```  
  
## Return Value  
 `TRUE` if the animation that occurs when a user expands or collapses a group is enabled; otherwise, `FALSE`.  
  
## Remarks  
 Call [CMFCTasksPane::EnableAnimation](../vs140/CMFCTasksPane--EnableAnimation.md) to enable or disable animation.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)