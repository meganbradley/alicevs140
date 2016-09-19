---
title: "CDockingManager::m_nTimeOutBeforeToolBarDock"
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
ms.assetid: f904eec3-8bd4-4010-9e07-482f0eeb6322
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::m_nTimeOutBeforeToolBarDock
Specifies the time, in milliseconds, before a toolbar is docked to the main frame window.  
  
## Syntax  
  
```  
static UINT m_nTimeOutBeforeToolBarDock;  
```  
  
## Remarks  
 Before a toolbar is docked, the framework waits the specified length of time. This prevents the toolbar from being accidentally docked to a location while the user is still dragging it.  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)