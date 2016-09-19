---
title: "CDockingManager::FixupVirtualRects"
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
ms.assetid: f3681766-e19f-4884-b831-23c7d04cb9a6
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::FixupVirtualRects
Commits all current toolbar positions to virtual rectangles.  
  
## Syntax  
  
```  
virtual void FixupVirtualRects();  
```  
  
## Remarks  
 When the user starts to drag a toolbar, the application remembers its original position in the *virtual rectangle*. When the user moves a toolbar across its dock site, the toolbar may shift other toolbars. The original positions of the other toolbars are stored in the corresponding virtual rectangles.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)