---
title: "COleControl::SetFocus"
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
ms.assetid: 53088ba1-b7ba-497c-a199-65ccdf8f6875
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetFocus
Causes the control's container window to take possession of the input focus on the control's behalf.  
  
## Syntax  
  
```  
  
CWnd* SetFocus( );  
```  
  
## Return Value  
 A pointer to the **CWnd** window object that previously had the input focus, or **NULL** if there is no such window.  
  
## Remarks  
 If the control is activated and windowless, this function causes the control's container window to take possession of the input focus, on the control's behalf. The input focus directs keyboard input to the container's window, and the container dispatches all subsequent keyboard messages to the OLE object that calls `SetFocus`. Any window that previously had the input focus loses it.  
  
 If the control is not windowless, this function causes the control itself to take possession of the input focus (same as `CWnd::SetFocus`).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetFocus](../vs140/COleControl--GetFocus.md)