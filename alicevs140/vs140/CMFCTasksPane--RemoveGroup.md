---
title: "CMFCTasksPane::RemoveGroup"
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
ms.assetid: a5ac7750-0bca-44dd-8ed1-698941feea9a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::RemoveGroup
Removes a group.  
  
## Syntax  
  
```  
void RemoveGroup(  
    int nGroup  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the group to remove.  
  
## Remarks  
 This method removes a single group. To remove all groups, call [CMFCTasksPane::RemoveAllGroups](../vs140/CMFCTasksPane--RemoveAllGroups.md) instead.  
  
 When the framework removes a group, all tasks and user windows associated with it are destroyed.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)