---
title: "CMFCTasksPane::SetTasksHorzOffset"
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
ms.assetid: 05721f8b-4b60-4185-988d-fa4167300fe9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetTasksHorzOffset
Sets the horizontal offset for tasks.  
  
## Syntax  
  
```  
void SetTasksHorzOffset(  
    int n = -1  
);  
```  
  
#### Parameters  
 [in] `n`  
 Specifies the horizontal offset.  
  
## Remarks  
 The horizontal offset is the distance in pixels from the left and right edges of a group.  
  
 If `n` is -1, this method sets the horizontal offset to the value returned by the `CMFCVisualManager::GetTasksPaneTaskHorzOffset` method.  
  
 The default horizontal offset is 12 pixels.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)