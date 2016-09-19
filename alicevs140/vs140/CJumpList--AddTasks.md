---
title: "CJumpList::AddTasks"
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
ms.assetid: 4f7891bc-95e9-4755-b156-1e1752b552e6
caps.latest.revision: 8
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CJumpList::AddTasks
Adds items to the canonical Tasks category.  
  
## Syntax  
  
```  
BOOL AddTasks(  
   IObjectArray* pObjectCollection  
);  
```  
  
#### Parameters  
 `pObjectCollection`  
 A collection of tasks to be added.  
  
## Return Value  
  
## Remarks  
 The instance of CJumpList accumulates specified tasks and adds them to the Destination List during `CommitList`. Task items will appear in a category at the bottom of the application's destination menu. This category takes precedence over all other categories when it is filled in the UI.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CJumpList](../vs140/CJumpList-Class.md)