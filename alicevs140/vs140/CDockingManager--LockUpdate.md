---
title: "CDockingManager::LockUpdate"
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
ms.assetid: 5e7abab6-95ca-4921-b3f7-9f7d3eec59c9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::LockUpdate
Locks the given window.  
  
## Syntax  
  
```  
void LockUpdate(  
   BOOL bLock  
);  
```  
  
#### Parameters  
 [in] `bLock`  
 `TRUE` if the window is locked; `FALSE` otherwise.  
  
## Remarks  
 When a window is locked, it cannot be moved and it cannot be redrawn.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)