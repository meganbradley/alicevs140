---
title: "CWnd::KillTimer"
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
ms.assetid: c4a11e5a-3215-4d96-8c3b-3934324cc3ff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::KillTimer
Kills the timer event identified by `nIDEvent` from the earlier call to `SetTimer`.  
  
## Syntax  
  
```  
  
      BOOL KillTimer(  
   UINT_PTR nIDEvent   
);  
```  
  
#### Parameters  
 `nIDEvent`  
 The value of the timer event passed to [SetTimer](../vs140/CWnd--SetTimer.md).  
  
## Return Value  
 Specifies the outcome of the function. The value is nonzero if the event was killed. It is 0 if the `KillTimer` member function could not find the specified timer event.  
  
## Remarks  
 Pending [WM_TIMER](../vs140/CWnd--OnTimer.md) messages associated with the timer are not removed from the message queue.  
  
## Example  
 See the example for [CWnd::SetTimer](../vs140/CWnd--SetTimer.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetTimer](../vs140/CWnd--SetTimer.md)   
 [KillTimer](http://msdn.microsoft.com/library/windows/desktop/ms644903)