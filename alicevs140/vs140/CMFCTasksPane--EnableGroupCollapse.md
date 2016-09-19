---
title: "CMFCTasksPane::EnableGroupCollapse"
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
ms.assetid: 3eef7be1-7f0d-4b06-a650-86f35452a5ae
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::EnableGroupCollapse
Specifies whether a user can collapse task groups.  
  
## Syntax  
  
```  
void EnableGroupCollapse(  
    BOOL bEnable  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` if users can collapse task groups; otherwise, `FALSE`.  
  
## Remarks  
 A task group that is collapsed displays only the group caption; the list of tasks is hidden.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)