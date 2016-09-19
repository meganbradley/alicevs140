---
title: "CMFCTabCtrl::m_bEnableActivate"
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
ms.assetid: dd0601aa-f729-4740-9411-756f9f57724c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::m_bEnableActivate
Prevents the active view from losing focus when a new tab is inserted and enabled.  
  
## Syntax  
  
```  
static BOOL m_bEnableActivate;  
```  
  
## Remarks  
 The focus is usually taken by a new tabbed window when the tab is inserted and made active. Set the `CMFCTabCtrl::m_bEnableActivate` member variable to `FALSE` to retain the original focus. The default value is `TRUE`.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)