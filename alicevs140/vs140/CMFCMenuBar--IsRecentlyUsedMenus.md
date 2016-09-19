---
title: "CMFCMenuBar::IsRecentlyUsedMenus"
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
ms.assetid: 2b7e14df-1427-47d3-93a5-b32ef2da7acd
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::IsRecentlyUsedMenus
Indicates whether recently used menu commands are displayed on the menu bar.  
  
## Syntax  
  
```  
static BOOL IsRecentlyUsedMenus();  
```  
  
## Return Value  
 Nonzero if the [CMFCMenuBar](../vs140/CMFCMenuBar-Class.md) object shows recently used menu commands; otherwise 0.  
  
## Remarks  
 Use the function [CMFCMenuBar::SetRecentlyUsedMenus](../vs140/CMFCMenuBar--SetRecentlyUsedMenus.md) to control whether the menu bar shows recently used menu commands.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::SetRecentlyUsedMenus](../vs140/CMFCMenuBar--SetRecentlyUsedMenus.md)