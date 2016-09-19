---
title: "CDockingManager::m_nTimeOutBeforeDockingBarDock"
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
ms.assetid: c8d087d5-763d-4735-b280-ad6ad883722e
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::m_nTimeOutBeforeDockingBarDock
Specifies the time, in milliseconds, before a docking pane is docked in immediate docking mode.  
  
## Syntax  
  
```  
static UINT m_nTimeOutBeforeDockingBarDock;  
```  
  
## Remarks  
 Before a pane is docked, the framework waits the specified length of time. This prevents the pane from being accidentally docked to a location while the user is still dragging it.  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)