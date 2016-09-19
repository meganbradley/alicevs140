---
title: "CBasePane::GetDockSiteFrameWnd"
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
ms.assetid: f7c7f794-2e5a-43b2-b78a-87d69443e4fb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetDockSiteFrameWnd
Returns a pointer to the [CDockingPanesRow](../vs140/CDockingPanesRow-Class.md)object where the pane is docked.  
  
## Syntax  
  
```  
virtual CWnd* GetDockSiteFrameWnd() const;  
```  
  
## Return Value  
 A pointer to the dock site of the pane.  
  
## Remarks  
 Call this method to retrieve a pointer to the dock site of the pane. The dock site can be either a main frame window if the pane is docked to the main frame, or a mini-frame window if the pane is floating.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)