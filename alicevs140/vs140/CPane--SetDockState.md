---
title: "CPane::SetDockState"
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
ms.assetid: 80a4e9f3-a1c5-4c5a-8d9b-becdcae3b88e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::SetDockState
Restores docking state information for the pane.  
  
## Syntax  
  
```  
virtual void SetDockState(  
   CDockingManager* pDockManager  
);  
```  
  
#### Parameters  
 [in] `pDockManager`  
 Pointer to the docking manager for the main frame window.  
  
## Remarks  
 This method is called by the framework to restore recent docking state information for the pane. A pane stores recent docking state information in [CPane::m_recentDockInfo](../vs140/CPane--m_recentDockInfo.md). For more information, see the [CRecentDockSiteInfo Class](../vs140/CRecentDockSiteInfo-Class.md).  
  
 You can also call this method to set the docking state when you load pane information from an external source.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPane::m_recentDockInfo](../vs140/CPane--m_recentDockInfo.md)   
 [CRecentDockSiteInfo Class](../vs140/CRecentDockSiteInfo-Class.md)