---
title: "CMFCTasksPane::RemoveAllGroups"
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
ms.assetid: b818c2bd-7fe4-4248-9982-f7a2fcf21989
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::RemoveAllGroups
Removes all groups on the specified page.  
  
## Syntax  
  
```  
void RemoveAllGroups(  
    int nPageIdx = 0  
);  
```  
  
#### Parameters  
 [in] `nPageIdx`  
 Specifies the zero-based index of the page.  
  
## Remarks  
 Removes all groups on the page specified by `nPageIdx`, or all groups if there is only a default page.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)