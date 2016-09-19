---
title: "CMFCTasksPane::AddGroup"
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
ms.assetid: 6e4131dc-9bc3-489a-9e28-0dfa79b2a5c3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::AddGroup
Adds a new group of tasks to the task pane control.  
  
## Syntax  
  
```  
int AddGroup(  
    int nPageIdx,  
    LPCTSTR lpszGroupName,  
    BOOL bBottomLocation = FALSE,  
    BOOL bSpecial = FALSE,  
    HICON hIcon = NULL  
);  
int AddGroup(  
    LPCTSTR lpszGroupName,  
    BOOL bBottomLocation = FALSE,  
    BOOL bSpecial = FALSE,  
    HICON hIcon = NULL  
);  
```  
  
#### Parameters  
 [in] `nPageIdx`  
 Specifies the zero-based page index.  
  
 [in] `lpszGroupName`  
 Specifies the group name.  
  
 [in] `bBottomLocation`  
 `TRUE` to create the group at the bottom of the task pane control; otherwise, `FALSE`.  
  
 [in] `bSpecial`  
 `TRUE` to mark this group as a *special* group; otherwise, `FALSE`. For more information about special groups, see the Remarks section of [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md).  
  
 [in] `hIcon`  
 Specifies the icon to display in the group caption.  
  
## Return Value  
 The zero-based index of the group in the internal list of groups that the class maintains.  
  
## Remarks  
 Call this method to create a group of tasks and to add that group to the task pane control.  
  
 The framework displays task groups at the top of the task pane control or at the bottom. The framework can display only one group at the bottom; this group must be added last.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)