---
title: "CPane::DockByMouse"
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
ms.assetid: 54952c79-b707-45fe-a2e1-247b8f539b47
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::DockByMouse
Docks a pane by using the mouse.  
  
## Syntax  
  
```  
virtual BOOL DockByMouse(  
   CBasePane* pDockBar  
);  
```  
  
#### Parameters  
 [in] `pDockBar`  
 Specifies the base pane to which to dock this pane.  
  
## Return Value  
 `TRUE` if the pane was docked successfully; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)