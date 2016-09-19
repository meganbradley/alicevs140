---
title: "CBasePane::DoesAllowDynInsertBefore"
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
ms.assetid: 394755fd-7f7d-4e3a-bbc0-b289c0637d58
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::DoesAllowDynInsertBefore
Determines whether another pane can be dynamically inserted between this pane and the parent frame.  
  
## Syntax  
  
```  
virtual BOOL DoesAllowDynInsertBefore() const;  
```  
  
## Return Value  
 `TRUE` if a user can insert another pane; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method to determine whether a user can dynamically insert a pane before this pane.  
  
 For example, suppose your application creates a pane docked at the left side of the frame (such as the Outlook bar). To prevent the user from docking another pane to the left of the first pane, override this method and return `FALSE`.  
  
 We recommend that you override this method and return `FALSE` for non-floating panes derived from [CDockablePane Class](../vs140/CDockablePane-Class.md).  
  
 The default implementation returns `TRUE`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)