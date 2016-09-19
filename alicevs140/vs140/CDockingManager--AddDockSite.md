---
title: "CDockingManager::AddDockSite"
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
ms.assetid: 78b1639d-7b96-4a12-8947-0cfde09f3f2d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::AddDockSite
Creates a dock pane and adds it to the list of control bars.  
  
## Syntax  
  
```  
BOOL AddDockSite(  
   const AFX_DOCKSITE_INFO& info,  
   CDockSite** ppDockBar = NULL  
);  
```  
  
#### Parameters  
 [in] `info`  
 A reference to an info structure that contains dock pane alignment.  
  
 [out] `ppDockBar`  
 A pointer to a pointer to the new dock pane.  
  
## Return Value  
 `TRUE` if the dock pane was created successfully; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)