---
title: "CDockingManager::RemoveMiniFrame"
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
ms.assetid: 4be1f622-4060-4895-afbc-affcb773b52b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::RemoveMiniFrame
Removes a specified frame from the list of mini frames.  
  
## Syntax  
  
```  
virtual BOOL RemoveMiniFrame(  
   CPaneFrameWnd* pWnd  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 A pointer to a frame to remove.  
  
## Return Value  
 `TRUE` if the specified frame is removed; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)