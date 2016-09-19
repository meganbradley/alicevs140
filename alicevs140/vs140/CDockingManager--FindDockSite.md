---
title: "CDockingManager::FindDockSite"
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
ms.assetid: 863c0e14-ae3d-4fe6-9ce7-38aa2ca8085e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::FindDockSite
Retrieves the bar pane that is at the specified position and that has the specified alignment.  
  
## Syntax  
  
```  
virtual CDockSite* FindDockSite(  
   DWORD dwAlignment,  
   BOOL bOuter  
);  
```  
  
#### Parameters  
 [in] `dwAlignment`  
 The alignment of the bar pane.  
  
 [in] `bOuter`  
 If `TRUE`, retrieve the bar in the head position in the list of control bars. Otherwise, retrieve the bar in the tail position in the list of control bars.  
  
## Return Value  
 The docking pane that has the specified alignment; `NULL` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)