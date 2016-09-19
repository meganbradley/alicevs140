---
title: "CMFCTasksPane::GetTaskLocation"
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
ms.assetid: db167269-e4da-41fc-b3c1-7841582395a8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::GetTaskLocation
Returns the group and the index for a specified task.  
  
## Syntax  
  
```  
BOOL GetTaskLocation(  
    UINT uiCommandID,  
    int& nGroup,  
    int& nTask  
) const;  
BOOL GetTaskLocation(  
    HWND hwndTask,  
    int& nGroup,  
    int& nTask  
) const;  
BOOL GetTaskLocation(  
    CMFCTasksPaneTask* pTask,  
    int& nGroup,  
    int& nTask  
) const;  
```  
  
#### Parameters  
 [in] `uiCommandID`  
 Specifies the command ID of the task to find.  
  
 [out] `nGroup`  
 Contains the group index of the task.  
  
 [out] `nTask`  
 Contains the index of the task in the task group.  
  
 [in] `hwndTask`  
 Specifies the window associated with the task.  
  
 [in] `pTask`  
 Specifies the task to find.  
  
## Return Value  
 `TRUE` if the task location was found; `FALSE` if the specified task does not exist.  
  
## Remarks  
 This method retrieves the group index and task index for the specified task. If the method returns `FALSE`, `nGroup` and `nTask` are set to -1.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)