---
title: "CBasePane::IsInFloatingMultiPaneFrameWnd"
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
ms.assetid: 1b6a6aec-9384-4efc-b0f4-10e16f2086e3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsInFloatingMultiPaneFrameWnd
Specifies whether the pane is in a multi-pane frame window ([CMultiPaneFrameWnd Class](../vs140/CMultiPaneFrameWnd-Class.md)).  
  
## Syntax  
  
```  
virtual BOOL IsInFloatingMultiPaneFrameWnd() const;  
```  
  
## Return Value  
 `TRUE` if the pane is in a multi-pane frame window; otherwise, `FALSE`.  
  
## Remarks  
 Only dockable panes can float in a multi-pane frame window. Therefore, `CBasePane::IsInFloatingMultiPaneFrameWnd` always returns `FALSE`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)