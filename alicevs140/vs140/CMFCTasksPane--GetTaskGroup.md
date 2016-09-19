---
title: "CMFCTasksPane::GetTaskGroup"
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
ms.assetid: 4273a1b2-3b64-4e29-ae78-60003bf579a3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::GetTaskGroup
Returns a task group for a specified group index.  
  
## Syntax  
  
```  
CMFCTasksPaneTaskGroup* GetTaskGroup(  
    int nGroup  
) const;  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the group to retrieve.  
  
## Return Value  
 The task group at the specified index.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCTasksPane::GetGroupLocation](../vs140/CMFCTasksPane--GetGroupLocation.md)