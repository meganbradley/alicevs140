---
title: "CEvent::ResetEvent"
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
ms.assetid: d78e2518-4347-4042-b0bf-2ed2240e395f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEvent::ResetEvent
Sets the state of the event to nonsignaled until explicitly set to signaled by the [SetEvent](../vs140/CEvent--SetEvent.md) member function.  
  
## Syntax  
  
```  
  
BOOL ResetEvent( );  
  
```  
  
## Return Value  
 Nonzero if the function was successful; otherwise 0.  
  
## Remarks  
 This causes all threads wishing to access this event to wait.  
  
 This member function is not used by automatic events.  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CEvent Class](../vs140/CEvent-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)