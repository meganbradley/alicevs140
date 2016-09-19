---
title: "CDockSite::PaneFromPoint"
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
ms.assetid: 1974ec34-99f5-4a01-a74d-3482b1d3692c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockSite::PaneFromPoint
Returns a pane that is docked in the dock site at the point specified by the given parameter.  
  
## Syntax  
  
```  
virtual CPane* PaneFromPoint(  
    CPoint pt   
);  
```  
  
#### Parameters  
 [in] `pt`  
 A point, in screen coordinates, for the pane to retrieve.  
  
## Return Value  
 A pointer to the pane located at the specified point or `NULL` if no pane was present at the specified point.  
  
## Remarks  
  
## Requirements  
 **Header:** afxDockSite.h  
  
## See Also  
 [CDockSite Class](../vs140/CDockSite-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)