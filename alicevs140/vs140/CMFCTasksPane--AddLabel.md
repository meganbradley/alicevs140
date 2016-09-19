---
title: "CMFCTasksPane::AddLabel"
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
ms.assetid: 6cbdd061-17c4-4b9a-b6a4-a6507b41358d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::AddLabel
Adds a label to the specified task group.  
  
## Syntax  
  
```  
int AddLabel(  
    int nGroup,  
    LPCTSTR lpszLabelName,  
    int nTaskIcon = -1,  
    BOOL bIsBold = FALSE  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the index of the group where the label is added.  
  
 [in] `lpszLabelName`  
 Specifies the name of the label.  
  
 [in] `nTaskIcon`  
 Specifies the icon to display next to the label. The framework stores icons in a list of images. This parameter is an index into that list.  
  
 [in] `bIsBold`  
 `TRUE` to display the label in bold text; otherwise, `FALSE`.  
  
## Return Value  
 The zero-based index of the group where the label was added, or -1 if the group specified by `nGroup` does not exist.  
  
## Remarks  
 The framework handles tasks and labels differently. When a user clicks on a task, the framework executes a command. When a user clicks on a label, no command is executed. For more information, see [CMFCTasksPane::AddTask](../vs140/CMFCTasksPane--AddTask.md).  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)