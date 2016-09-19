---
title: "CMFCTasksPane::OnClickTask"
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
ms.assetid: 25c26b67-e3dc-47eb-9c00-047a56614226
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::OnClickTask
Called by the framework when the user clicks an item in the task pane.  
  
## Syntax  
  
```  
virtual void OnClickTask(  
    int nGroupNumber,  
    int nTaskNumber,  
    UINT uiCommandID,  
    DWORD dwUserData  
);  
```  
  
#### Parameters  
 [in] `nGroupNumber`  
 Specifies the zero-based index of the group that contains the clicked task.  
  
 [in] `nTaskNumber`  
 Specifies the zero-based index of the clicked task.  
  
 [in] `uiCommandID`  
 Specifies the command ID associated with the task.  
  
 [in] `dwUserData`  
 Contains user-defined data associated with the clicked task.  
  
## Remarks  
 The framework calls this method when a user clicks a task. By default, the framework checks the command ID associated with the clicked task and, if it is not zero, sends the `WM_COMMAND` message to the owner of the task pane control.  
  
 Override this method in a derived class to execute custom code when a task is clicked.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)