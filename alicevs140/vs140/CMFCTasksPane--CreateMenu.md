---
title: "CMFCTasksPane::CreateMenu"
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
ms.assetid: 364ed1fa-98fe-4253-b46b-fd1b61969ae2
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTasksPane::CreateMenu
Creates a menu that appears when a user clicks the **Other Tasks Panes** menu button.  
  
## Syntax  
  
```  
HMENU CreateMenu() const;  
```  
  
## Return Value  
 A handle to the new menu.  
  
## Remarks  
 Override this method in a derived class to customize the menu for a task pane.  
  
 The pop-up menu  that this method creates contains the list of pages in the task pane. The menu displays a check mark next to the active page.  
  
## Requirements  
 **Header:** afxTasksPane.h  
  
## See Also  
 [CMFCTasksPane Class](../vs140/CMFCTasksPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)