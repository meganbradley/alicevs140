---
title: "CDockingManager::FindPaneByID"
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
ms.assetid: 1cada873-dcb9-4a69-95ef-bf354775a12a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::FindPaneByID
Finds a pane by the specified control ID.  
  
## Syntax  
  
```  
virtual CBasePane* FindPaneByID(  
    UINT uBarID,  
    BOOL bSearchMiniFrames = FALSE  
);  
```  
  
#### Parameters  
 [in] `uBarID`  
 Specifies the control ID of the pane to find.  
  
 [in] `bSearchMiniFrames`  
 `TRUE` to include all floating panes in the search. `FALSE` to include only the docked panes.  
  
## Return Value  
 The [CBasePane](../vs140/CBasePane-Class.md) object that has the specified control ID, or `NULL` if the specified pane cannot be found.  
  
## Remarks  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)