---
title: "CBasePane::SetDockingMode"
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
ms.assetid: ef8e450c-9b4f-45f2-9d2f-f0f85dd285d4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::SetDockingMode
Sets the docking mode for the pane.  
  
## Syntax  
  
```  
void SetDockingMode(  
   AFX_DOCK_TYPE dockModeNew  
);  
```  
  
#### Parameters  
 [in] `dockModeNew`  
 Specifies the new docking mode for the pane.  
  
## Remarks  
 The framework supports two docking modes: standard and immediate.  
  
 In the standard docking mode, panes and mini-frame windows are moved around using a drag rectangle. In the immediate docking mode, control bars and mini-frame windows are moved immediately with their context.  
  
 Initially, the docking mode is defined globally by [CDockingManager::m_dockModeGlobal](../vs140/CDockingManager--m_dockModeGlobal.md). You can set the docking mode for each pane individually using the `SetDockingMode` method.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CBasePane::GetDockingMode](../vs140/CBasePane--GetDockingMode.md)