---
title: "CBaseTabbedPane::HasAutoHideMode"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: b344f6de-13a2-4847-85b2-ec1042b98209
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::HasAutoHideMode
Determines whether the tabbed pane can be switched to autohide mode.  
  
## Syntax  
  
```  
virtual BOOL HasAutoHideMode() const;  
```  
  
## Return Value  
 `TRUE` if the pane can be switched to autohide mode; otherwise, `FALSE`.  
  
## Remarks  
 If autohide mode is disabled, no pin button is displayed on the tabbed pane caption.  
  
## Requirements  
 **Header:** afxBaseTabbedPane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)