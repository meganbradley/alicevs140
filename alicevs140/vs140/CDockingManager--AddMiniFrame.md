---
title: "CDockingManager::AddMiniFrame"
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
ms.assetid: c1452ecc-ff21-4695-a673-d161bd869dad
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::AddMiniFrame
Adds a frame to the list of mini frames.  
  
## Syntax  
  
```  
virtual BOOL AddMiniFrame(  
   CPaneFrameWnd* pWnd  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 A pointer to a frame.  
  
## Return Value  
 `TRUE` if the frame is not in the list of mini frames and was added successfully; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)