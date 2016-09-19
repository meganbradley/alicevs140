---
title: "CDockingManager::GetPaneList"
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
ms.assetid: a258b61d-8774-4412-8b72-4fbf92d0b239
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::GetPaneList
Returns a list of panes that belong to the docking manager. This includes all floating panes.  
  
## Syntax  
  
```  
void GetPaneList(  
    CObList& lstBars,  
    BOOL bIncludeAutohide = FALSE,  
    CRuntimeClass* pRTCFilter = NULL,  
    BOOL bIncludeTabs = FALSE  
);  
```  
  
#### Parameters  
 [in, out] `lstBars`  
 Contains all the panes of the current docking manager.  
  
 [in] `bIncludeAutohide`  
 `TRUE` to include the panes that are in autohide mode; otherwise, `FALSE`.  
  
 [in] `pRTCFilter`  
 If not `NULL`, the returned list contains panes only of the specified runtime class.  
  
 [in] `bIncludeTabs`  
 `TRUE` to include tabs; otherwise, `FALSE`.  
  
## Remarks  
 If there are any tabbed panes in the docking manager, the method returns pointers to [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md) objects and you must enumerate the tabs explicitly.  
  
 Use `pRTCFilter` to obtain a particular class of panes. For example, you can obtain only toolbars by setting this value appropriately.  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)