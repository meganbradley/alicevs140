---
title: "CBasePane::IsDocked"
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
ms.assetid: 65a26c49-032d-4b27-b07f-904f7de96f76
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::IsDocked
Determines whether the pane is docked.  
  
## Syntax  
  
```  
virtual BOOL IsDocked() const;  
```  
  
## Return Value  
 `TRUE` if the parent of the pane is not a mini-frame or if the pane is floating in a mini-frame with another pane; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)