---
title: "CDockablePane::CanAutoHide"
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
ms.assetid: 27d253ef-77aa-4d66-bfc8-4df38d53670a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::CanAutoHide
Determines whether the pane can auto-hide.  
  
## Syntax  
  
```  
virtual BOOL CanAutoHide() const;  
```  
  
## Return Value  
 `TRUE` if the pane can auto-hide; otherwise, `FALSE`.  
  
## Remarks  
 `CDockablePane::CanAutoHide` returns `FALSE` in any of the following situations:  
  
-   The pane has no parent.  
  
-   The docking manager does not allow panes to auto-hide.  
  
-   The pane is not docked.  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)