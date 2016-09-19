---
title: "CMFCTasksPane::ShowTaskByCmdId"
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
ms.assetid: 455a847c-1ce9-418c-95c8-8dc6f775c466
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::ShowTaskByCmdId
Shows or hides a task based on its command ID.  
  
## Syntax  
  
```  
BOOL ShowTaskByCmdId(  
    UINT uiCommandID,  
    BOOL bShow = TRUE,  
    BOOL bRedraw = TRUE  
);  
```  
  
#### Parameters  
 [in] `uiCommandID`  
 Specifies the command ID of the task to show or hide.  
  
 [in] `bShow`  
 `TRUE` to show the task; `FALSE` to hide the task.  
  
 [in] `bRedraw`  
 `TRUE` to redraw the task pane; otherwise, `FALSE`.  
  
## Return Value  
 `TRUE` if the task was successfully shown or hidden; `FALSE` if a task with the specified command ID does not exist.  
  
## Remarks  
 Use [CMFCTasksPane::ShowTask](../vs140/CMFCTasksPane--ShowTask.md) to show or hide a task based on its command ID.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)