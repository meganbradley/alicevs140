---
title: "CDockablePane::DockToRecentPos"
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
ms.assetid: 20819147-51e5-48cf-b64c-c9aeea02b413
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::DockToRecentPos
Docks a pane to its stored docking position.  
  
## Syntax  
  
```  
BOOL CDockablePane::DockToRecentPos();  
```  
  
## Return Value  
 `TRUE` if the pane is successfully docked; otherwise, `FALSE`.  
  
## Remarks  
 Dockable panes store recent docking information in a [CRecentDockSiteInfo](../vs140/CRecentDockSiteInfo-Class.md) object.  
  
## Requirements  
 **Header:**  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecentDockSiteInfo Class](../vs140/CRecentDockSiteInfo-Class.md)