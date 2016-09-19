---
title: "CPane::OnShowControlBarMenu"
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
ms.assetid: 920e17d6-26b1-4f44-b1fa-b3ad8f165b00
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::OnShowControlBarMenu
Called by the framework when a special pane menu is about to be displayed.  
  
## Syntax  
  
```  
virtual BOOL OnShowControlBarMenu(  
    CPoint point  
);  
```  
  
#### Parameters  
 [in] `point`  
 Specifies the menu location.  
  
## Return Value  
 `TRUE` if the menu can be displayed; otherwise, `FALSE`.  
  
## Remarks  
 The menu contains several items that enable you to specify the pane's behavior, namely: **Floating**, **Docking**, **AutoHide**, and **Hide**. You can enable this menu for all panes by calling [CDockingManager::EnableDockSiteMenu](../vs140/CDockingManager--EnableDockSiteMenu.md).  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)