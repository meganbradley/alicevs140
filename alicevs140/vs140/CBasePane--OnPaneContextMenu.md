---
title: "CBasePane::OnPaneContextMenu"
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
ms.assetid: cbc584dd-848d-4ecc-a0e2-32c737bec474
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::OnPaneContextMenu
Called by the framework when it builds a menu that has a list of panes.  
  
## Syntax  
  
```  
virtual void OnPaneContextMenu(  
   CWnd* pParentFrame,  
   CPoint point  
);  
```  
  
#### Parameters  
 [in] `pParentFrame`  
 A pointer to the parent frame.  
  
 [in] `point`  
 Specifies the location of the shortcut menu.  
  
## Remarks  
 `OnPaneContextMenu` calls the docking manager, which maintains the list of panes that belong to the current frame window. This method adds the names of the panes to a shortcut menu and displays it. The commands on the menu show or hide individual panes.  
  
 Override this method to customize this behavior.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)