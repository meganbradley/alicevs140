---
title: "CDockingManager::BuildPanesMenu"
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
ms.assetid: 693decf2-beae-4ca3-b740-2ff05231eed0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::BuildPanesMenu
Adds names of docking panes and toolbars to a menu.  
  
## Syntax  
  
```  
void BuildPanesMenu(  
   CMenu& menu,  
   BOOL bToolbarsOnly  
);  
```  
  
#### Parameters  
 [in] `menu`  
 A menu to add the names of docking panes and toolbars to.  
  
 [in] `bToolbarsOnly`  
 `TRUE` to add only toolbar names to the menu; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)