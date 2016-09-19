---
title: "CMFCTasksPane::SetGroupCaptionHeight"
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
ms.assetid: bb7783f9-eb33-48e9-8da6-c4deaf598390
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetGroupCaptionHeight
Sets the height of a group caption.  
  
## Syntax  
  
```  
void SetGroupCaptionHeight(  
    int n = -1  
);  
```  
  
#### Parameters  
 [in] `n`  
 Specifies the caption height.  
  
## Remarks  
 Call this method to customize the margins of the task pane elements.  
  
 If `n` is -1, the framework determines the margin value by using the visual manager (`CMFCVisualManager::GetTasksPaneGroupCaptionHeight`). The default caption height is 25 pixels.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)