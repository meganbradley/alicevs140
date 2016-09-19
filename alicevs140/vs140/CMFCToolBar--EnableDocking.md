---
title: "CMFCToolBar::EnableDocking"
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
ms.assetid: ea8adf4b-d0cd-418c-8f5f-5a981e8e7503
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::EnableDocking
Enables docking of the pane to the main frame.  
  
## Syntax  
  
```  
virtual void EnableDocking(  
   DWORD dwAlignment  
);  
```  
  
#### Parameters  
 [in] `dwAlignment`  
 Specifies the docking alignment to enable.  
  
## Remarks  
 This method extends the base class implementation, [CBasePane::EnableDocking](../vs140/CBasePane--EnableDocking.md), by setting the `CBasePane::m_dwControlBarStyle` data member to `AFX_CBRS_FLOAT`. This method then passes `dwAlignment` to the base class implementation.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CBasePane::EnableDocking](../vs140/CBasePane--EnableDocking.md)