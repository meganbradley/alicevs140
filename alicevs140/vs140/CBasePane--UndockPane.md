---
title: "CBasePane::UndockPane"
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
ms.assetid: 412045c9-3b5f-4a72-b196-006d33a89708
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::UndockPane
Removes the pane from the dock site, default slider, or mini-frame window where it is currently docked.  
  
## Syntax  
  
```  
virtual void UndockPane(  
   BOOL bDelay=FALSE  
);  
```  
  
#### Parameters  
 `bDelay`  
 If TRUE, the docking layout is not recalculated immediately.  
  
## Remarks  
 Call this method to manipulate the pane state or exclude the pane from the docking layout.  
  
 If you want to continue to use this pane, call either [CBasePane::DockPane](../vs140/CBasePane--DockPane.md) or [CBasePane::FloatPane](../vs140/CBasePane--FloatPane.md) before calling this method.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)