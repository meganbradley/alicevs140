---
title: "CBasePane::CanBeAttached"
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
ms.assetid: 3142b024-6481-4bfe-8882-a3a348785d9a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::CanBeAttached
Determines whether the pane can be docked to another pane or frame window.  
  
## Syntax  
  
```  
virtual BOOL CanBeAttached() const;  
```  
  
## Return Value  
 `TRUE` if the pane can be docked to another pane or frame window; otherwise `FALSE`.  
  
## Remarks  
 The default implementation returns `FALSE`. Override this method in a derived class to enable or disable the ability to dock without calling [CBasePane::EnableDocking](../vs140/CBasePane--EnableDocking.md).  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)