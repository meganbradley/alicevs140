---
title: "CMFCTasksPane::SetTaskTextColor"
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
ms.assetid: 3a90d955-b0f2-4667-9102-8882db3e1249
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetTaskTextColor
Sets the text color for a task.  
  
## Syntax  
  
```  
BOOL SetTaskTextColor(  
    int nGroup,  
    int nTask,  
    COLORREF color,  
    COLORREF colorHot = (COLORREF)-1  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the task group that contains the task.  
  
 [in] `nTask`  
 Specifies the zero-based index of the task.  
  
 [in] `color`  
 Specifies the text color for the task.  
  
 [in] `colorHot`  
 Specifies the text color for the highlighted group. If -1, this method uses the default highlight color.  
  
## Return Value  
 `TRUE` if the text color for the task was successfully set; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)