---
title: "CBasePane::GetParentTabWnd"
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
ms.assetid: 22e3fb79-dd0d-46b7-bd62-14f6e673566c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetParentTabWnd
Returns a pointer to the parent window that is inside a tab.  
  
## Syntax  
  
```  
CMFCBaseTabCtrl* GetParentTabWnd(  
   HWND& hWndTab  
) const;  
```  
  
#### Parameters  
 [out] `hWndTab`  
 If the return value is not `NULL`, this parameter contains the handle to the parent tabbed window.  
  
## Return Value  
 A valid pointer to the parent tabbed window or `NULL`.  
  
## Remarks  
 Use this function to retrieve a pointer to the parent tabbed window. Sometimes it is not enough to call `GetParent`, because a pane may be inside a docking wrapper ([CDockablePaneAdapter Class](../vs140/CDockablePaneAdapter-Class.md)) or inside a pane adapter ([CDockablePaneAdapter Class](../vs140/CDockablePaneAdapter-Class.md)). By using `GetParentTabWnd` you will be able to retrieve a valid pointer in those cases (assuming that the parent is a tabbed window).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)