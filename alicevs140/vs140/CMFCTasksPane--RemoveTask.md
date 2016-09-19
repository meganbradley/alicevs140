---
title: "CMFCTasksPane::RemoveTask"
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
ms.assetid: d5ded6a5-559f-4507-8ba5-c486df2459ba
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::RemoveTask
Removes a task from a task group.  
  
## Syntax  
  
```  
BOOL RemoveTask(  
    int nGroup,  
    int nTask,  
    BOOL bRedraw = TRUE  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the task group that contains the task to remove.  
  
 [in] `nTask`  
 Specifies the zero-based index of the task to remove.  
  
 [in] `bRedraw`  
 `TRUE` to redraw the task pane; otherwise, `FALSE`.  
  
## Return Value  
 `TRUE` if the function succeeds; `FALSE` if `nGroup` or `nTask` is invalid.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)