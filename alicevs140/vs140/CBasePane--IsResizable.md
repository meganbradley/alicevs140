---
title: "CBasePane::IsResizable"
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
ms.assetid: 2ae45130-1bac-496a-9d16-3c0c18f3a5a0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsResizable
Determines whether the pane can be resized.  
  
## Syntax  
  
```  
virtual BOOL IsResizable() const;  
```  
  
## Return Value  
 `TRUE` if the pane can be resized by the user; otherwise, `FALSE`.  
  
## Remarks  
 Panes of [CDockablePane Class](../vs140/CDockablePane-Class.md) can be resized.  
  
 The status bar ([CMFCStatusBar Class](../vs140/CMFCStatusBar-Class.md)) and the dock bar ([CDockSite Class](../vs140/CDockSite-Class.md)) cannot be resized.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)