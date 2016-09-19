---
title: "CEvent::PulseEvent"
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
ms.assetid: 576a525f-3d88-428a-acb7-7d7a8437328f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEvent::PulseEvent
Sets the state of the event to signaled (available), releases any waiting threads, and resets it to nonsignaled (unavailable) automatically.  
  
## Syntax  
  
```  
  
BOOL PulseEvent( );  
  
```  
  
## Return Value  
 Nonzero if the function was successful; otherwise 0.  
  
## Remarks  
 If the event is manual, all waiting threads are released, the event is set to nonsignaled, and `PulseEvent` returns. If the event is automatic, a single thread is released, the event is set to nonsignaled, and `PulseEvent` returns.  
  
 If no threads are waiting, or no threads can be released immediately, `PulseEvent` sets the state of the event to nonsignaled and returns.  
  
 `PulseEvent` uses the underlying Win32 `PulseEvent` function, which can be momentarily removed from the wait state by a kernel-mode asynchronous procedure call. Therefore, `PulseEvent` is unreliable and should not be used by new applications. For more information, see the [PulseEvent function](http://msdn.microsoft.com/library/windows/desktop/ms684914).  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CEvent Class](../vs140/CEvent-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)