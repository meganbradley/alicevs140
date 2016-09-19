---
title: "CMFCTasksPane::SetTaskName"
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
ms.assetid: 43b20d4a-67c2-421a-a4db-df1bda112480
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetTaskName
Sets the name for a task.  
  
## Syntax  
  
```  
BOOL SetTaskName(  
    int nGroup,  
    int nTask,  
    LPCTSTR lpszTaskName  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the task group.  
  
 [in] `nTask`  
 Specifies the zero-based index of the task.  
  
 [in] `lpszTaskName`  
 Specifies the task name.  
  
## Return Value  
 `TRUE` if the task name was successfully set; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)