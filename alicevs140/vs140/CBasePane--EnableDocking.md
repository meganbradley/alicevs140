---
title: "CBasePane::EnableDocking"
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
ms.assetid: 4f636957-839a-4bfe-bfd1-aad671600b1a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::EnableDocking
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
 Call this method to enable docking alignment to the main frame. You can pass a combination of `CBRS_ALIGN_` flags (for more information, see [CControlBar::EnableDocking](../vs140/CControlBar--EnableDocking.md)).  
  
 `EnableDocking` sets the internal flag `CBasePane::m_dwEnabledAlignment` and the framework checks this flag when a pane is docked.  
  
 Call [CBasePane::GetEnabledAlignment](../vs140/CBasePane--GetEnabledAlignment.md) to determine the docking alignment for a pane.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)