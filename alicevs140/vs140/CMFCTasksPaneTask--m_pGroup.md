---
title: "CMFCTasksPaneTask::m_pGroup"
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
ms.assetid: 67f99e13-583f-4161-8569-7914436c2714
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPaneTask::m_pGroup
Pointer to the [CMFCTasksPaneTaskGroup](../vs140/CMFCTasksPaneTaskGroup-Class.md) to which this task belongs.  
  
## Syntax  
  
```  
CMFCTasksPaneTaskGroup* m_pGroup;  
```  
  
## Remarks  
 Every task must have a parent group. You add groups to a task pane by calling [CMFCTasksPane::AddGroup](../vs140/CMFCTasksPane--AddGroup.md).  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCTasksPaneTask Class](../vs140/CMFCTasksPaneTask-Class.md)   
 [CMFCTasksPaneTaskGroup Class](../vs140/CMFCTasksPaneTaskGroup-Class.md)