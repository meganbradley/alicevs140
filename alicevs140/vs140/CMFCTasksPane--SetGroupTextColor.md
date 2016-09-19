---
title: "CMFCTasksPane::SetGroupTextColor"
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
ms.assetid: 34b10f83-a554-44ed-ba3f-97312629c0c0
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetGroupTextColor
Sets the text color for a group caption.  
  
## Syntax  
  
```  
BOOL SetGroupTextColor(  
    int nGroup,  
    COLORREF color,  
    COLORREF colorHot = (COLORREF)-1  
);  
```  
  
#### Parameters  
 [in] `nGroup`  
 Specifies the zero-based index of the group.  
  
 [in] `color`  
 Specifies the text color.  
  
 [in] `colorHot`  
 Specifies the text color for the highlighted group. If -1, the default highlight color is used.  
  
## Return Value  
 `TRUE` if the group text color was successfully changed; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)