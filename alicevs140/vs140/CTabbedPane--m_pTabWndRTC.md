---
title: "CTabbedPane::m_pTabWndRTC"
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
ms.assetid: 64d510c5-47d7-46af-b672-33e5e9914462
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabbedPane::m_pTabWndRTC
Runtime class information for a custom `CMFCTabCtrl`-derived object.  
  
## Syntax  
  
```  
AFX_IMPORT_DATA static CRuntimeClass* m_pTabWndRTC;  
```  
  
## Remarks  
 Set this static member variable to a pointer to the runtime class information of a `CMFCTabCtrl`-derived object if you are using a custom tabbed window inside a tabbed pane.  
  
## Requirements  
 **Header:** afxTabbedPane.h  
  
## See Also  
 [CTabbedPane Class](../vs140/CTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)