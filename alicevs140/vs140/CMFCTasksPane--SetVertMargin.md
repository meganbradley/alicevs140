---
title: "CMFCTasksPane::SetVertMargin"
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
ms.assetid: 8099d42b-aaa9-44e6-a3e1-488a9ea4c4f7
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetVertMargin
Sets the vertical margin.  
  
## Syntax  
  
```  
void SetVertMargin(  
    int n = -1  
);  
```  
  
#### Parameters  
 [in] `n`  
 Specifies the vertical margin to set.  
  
## Remarks  
 The vertical margin is the distance between a task pane and the vertical edges of the client area.  
  
 If `n` is -1, the framework determines the margin value by using  the visual manager (`CMFCVisualManager::GetTasksPaneVertMargin`). The default margin is 12 pixels.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)