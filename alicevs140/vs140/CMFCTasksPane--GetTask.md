---
title: "CMFCTasksPane::GetTask"
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
ms.assetid: 17861f54-b9d8-47e8-be2b-252c6c2534d3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::GetTask
Retrieves a task.  
  
## Syntax  
  
```  
CMFCTasksPaneTask* GetTask(  
    int nGroup,  
    int nTask  
) const;  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the group that contains the task.  
  
 [in] `nTask`  
 Specifies the zero-based index of the task in the list specified by `nGroup`.  
  
## Return Value  
 The task at the specified index.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCTasksPane::GetTaskLocation](../vs140/CMFCTasksPane--GetTaskLocation.md)