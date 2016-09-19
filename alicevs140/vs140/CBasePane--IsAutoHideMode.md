---
title: "CBasePane::IsAutoHideMode"
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
ms.assetid: 93509221-02fe-4993-ae62-e0b3b4cbbf98
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsAutoHideMode
Determines whether a pane is in auto-hide mode.  
  
## Syntax  
  
```  
virtual BOOL IsAutoHideMode() const;  
```  
  
## Return Value  
 `TRUE` if the pane is in auto-hide mode; otherwise, `FALSE`.  
  
## Remarks  
 Base panes cannot auto-hide. This method always returns `FALSE`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)