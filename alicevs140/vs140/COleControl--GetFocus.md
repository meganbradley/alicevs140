---
title: "COleControl::GetFocus"
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
ms.assetid: e1c6772d-172a-4c03-9c2a-405661fbc96d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetFocus
Determines whether the `COleControl` object has the focus.  
  
## Syntax  
  
```  
  
CWnd* GetFocus( );  
```  
  
## Return Value  
 If the control is activated and windowless, returns **this** if the control currently has the keyboard focus (as determined by the control's container), or **NULL** if it does not have the focus.  
  
 Otherwise, returns the `CWnd` object that has the focus (same as `CWnd::GetFocus`).  
  
## Remarks  
 An activated windowless control receives the focus when [SetFocus](../vs140/COleControl--SetFocus.md) is called.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetFocus](../vs140/COleControl--SetFocus.md)