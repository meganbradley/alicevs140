---
title: "CMFCTasksPane::SetActivePage"
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
ms.assetid: 61a86e1f-931f-4a92-af4c-82801ebaae8a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::SetActivePage
Makes the specified page in the task pane active.  
  
## Syntax  
  
```  
void SetActivePage(  
    int nPageIdx  
);  
```  
  
#### Parameters  
 [in] `nPageIdx`  
 Specifies the zero-based index of the page to display.  
  
## Remarks  
 This method asserts if the `nPageIdx` is invalid.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)