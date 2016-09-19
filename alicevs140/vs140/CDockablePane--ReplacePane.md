---
title: "CDockablePane::ReplacePane"
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
ms.assetid: dfb7ad8c-eb32-46e3-b647-e32f76033d80
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePane::ReplacePane
Replaces the pane with a specified pane.  
  
## Syntax  
  
```  
BOOL ReplacePane(  
   CDockablePane* pBarToReplaceWith,  
   AFX_DOCK_METHOD dockMethod,  
   BOOL bRegisterWithFrame = FALSE  
);  
```  
  
#### Parameters  
 [in] `pBarToReplaceWith`  
 A pointer to a dockable pane.  
  
 [in] `dockMethod`  
 Not used.  
  
 [in] `bRegisterWithFrame`  
 If `TRUE`, the new pane is registered with the docking manager of the parent of the old pane. The new pane is inserted at the index of the old pane in the list of panes that is maintained by the docking manager.  
  
## Return Value  
 `TRUE` if the replacement is successful; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxdockablepane.h  
  
## See Also  
 [CDockablePane Class](../vs140/CDockablePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)