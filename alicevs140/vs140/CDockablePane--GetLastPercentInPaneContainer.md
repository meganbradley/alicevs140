---
title: "CDockablePane::GetLastPercentInPaneContainer"
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
ms.assetid: 5e63a621-bff8-45b2-9f81-9b3d330fdb30
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::GetLastPercentInPaneContainer
Retrieves the percentage of space that a pane occupies in its container ([CPaneContainer Class](../vs140/CPaneContainer-Class.md)).  
  
## Syntax  
  
```  
int GetLastPercentInPaneContainer() const;  
```  
  
## Return Value  
 An `int` that specifies the percentage of space that the pane occupies in its container.  
  
## Remarks  
 This method is used when the container adjusts its layout.  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPaneContainer Class](../vs140/CPaneContainer-Class.md)