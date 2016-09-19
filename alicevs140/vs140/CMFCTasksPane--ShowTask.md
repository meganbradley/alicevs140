---
title: "CMFCTasksPane::ShowTask"
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
ms.assetid: a3dc34cf-64db-433c-8c7e-26e6c98b8458
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::ShowTask
Shows or hides a task.  
  
## Syntax  
  
```  
BOOL ShowTask(  
    int nGroup,  
    int nTask,  
    BOOL bShow = TRUE,  
    BOOL bRedraw = TRUE  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the group.  
  
 [in] `nTask`  
 Specifies the zero-based index of the task to show or hide.  
  
 [in] `bShow`  
 `TRUE` to show the task; `FALSE` to hide the task.  
  
 [in] `bRedraw`  
 `TRUE` to redraw the task pane; otherwise, `FALSE`.  
  
## Return Value  
 `TRUE` if the task was successfully shown or hidden; `FALSE` if the specified group or task does not exist.  
  
## Remarks  
 Use [CMFCTasksPane::ShowTaskByCmdId](../vs140/CMFCTasksPane--ShowTaskByCmdId.md) to show or hide a task based on its command ID.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)