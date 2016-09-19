---
title: "CBasePane::CanFocus"
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
ms.assetid: 22f06164-93a7-4b18-8d82-e5f5f22c1c9e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::CanFocus
Specifies whether the pane can receive focus.  
  
## Syntax  
  
```  
virtual BOOL CanFocus() const;  
```  
  
## Return Value  
 `TRUE` if the pane can receive focus; otherwise `FALSE`.  
  
## Remarks  
 Override this method in a derived class to control focus. For example, because toolbars cannot receive focus, this method returns `FALSE` when it is called on toolbar objects.  
  
 The framework tries to set the input focus when a pane is docked or floated.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)