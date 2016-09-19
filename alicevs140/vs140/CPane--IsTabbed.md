---
title: "CPane::IsTabbed"
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
ms.assetid: 00792a6e-4bd0-486c-9ae5-4bc614c07fc0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::IsTabbed
Determines whether the pane has been inserted into the tab control of a tabbed window.  
  
## Syntax  
  
```  
virtual BOOL IsTabbed() const;  
```  
  
## Return Value  
 `TRUE` if the pane is tabbed; otherwise, `FALSE`.  
  
## Remarks  
 The tabbed state is treated separately from the floating, docked, and auto-hide states.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)