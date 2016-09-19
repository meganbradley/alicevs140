---
title: "CDockingManager::InsertDockSite"
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
ms.assetid: 3e6f6b98-b6be-40ff-9280-951dc8bce5e9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::InsertDockSite
Creates a dock pane and inserts it into the list of control bars.  
  
## Syntax  
  
```  
BOOL InsertDockSite(  
   const AFX_DOCKSITE_INFO& info,  
   DWORD dwAlignToInsertAfter,  
   CDockSite** ppDockBar = NULL  
);  
```  
  
#### Parameters  
 [in] `info`  
 A structure that contains the alignment information about the dock pane.  
  
 [in] `dwAlignToInsertAfter`  
 Alignment of the dock pane.  
  
 [out] `ppDockBar`  
 A pointer to a pointer to a dock pane.  
  
## Return Value  
 `TRUE` if the dock pane was created successfully; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)