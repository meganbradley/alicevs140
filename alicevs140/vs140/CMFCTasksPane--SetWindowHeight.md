---
title: "CMFCTasksPane::SetWindowHeight"
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
ms.assetid: 93d1273a-f8c0-4333-8f17-ac396d119868
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetWindowHeight
Sets the height for a window control.  
  
## Syntax  
  
```  
BOOL SetWindowHeight(  
    int nGroup,  
    HWND hwndTask,  
    int nWndHeight  
);  
BOOL SetWindowHeight(  
    HWND hwndTask,  
    int nWndHeight  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the group that contains the window control.  
  
 [in] `hwndTask`  
 Specifies the handle to the window control.  
  
 [in] `nWndHeight`  
 Specifies the height to set.  
  
## Return Value  
 `TRUE` if the height of the window control was successfully set; `FALSE` if `nGroup` is invalid or if `hwndTask` does not exist.  
  
## Remarks  
 Call [CMFCTasksPane::AddWindow](../vs140/CMFCTasksPane--AddWindow.md) to add tasks with window controls.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)