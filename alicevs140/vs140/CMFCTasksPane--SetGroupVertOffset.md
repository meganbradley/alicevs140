---
title: "CMFCTasksPane::SetGroupVertOffset"
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
ms.assetid: c3e73d0b-8b52-4b27-9dd7-0def1d0c4334
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetGroupVertOffset
Sets the vertical offset for a group.  
  
## Syntax  
  
```  
void SetGroupVertOffset(  
    int n = -1  
);  
```  
  
#### Parameters  
 [in] `n`  
 Specifies the vertical offset.  
  
## Remarks  
 The vertical offset is the distance between a task group and the border of the task pane.  
  
 Call this method to customize the margins of task pane elements. If `n` is -1, the framework determines the margin value by using the visual manager (`CMFCVisualManager::GetTasksPaneGroupVertOffset`). The default offset is 15 pixels.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)