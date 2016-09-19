---
title: "CWinThread::OnIdle"
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
ms.assetid: d0ae16c9-4ade-4572-bd93-b46a3fdef726
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::OnIdle
Override this member function to perform idle-time processing.  
  
## Syntax  
  
```  
  
      virtual BOOL OnIdle(  
   LONG lCount   
);  
```  
  
#### Parameters  
 `lCount`  
 A counter incremented each time `OnIdle` is called when the thread's message queue is empty. This count is reset to 0 each time a new message is processed. You can use the `lCount` parameter to determine the relative length of time the thread has been idle without processing a message.  
  
## Return Value  
 Nonzero to receive more idle processing time; 0 if no more idle processing time is needed.  
  
## Remarks  
 `OnIdle` is called in the default message loop when the thread's message queue is empty. Use your override to call your own background idle-handler tasks.  
  
 `OnIdle` should return 0 to indicate that no additional idle processing time is required. The `lCount` parameter is incremented each time `OnIdle` is called when the message queue is empty and is reset to 0 each time a new message is processed. You can call your different idle routines based on this count.  
  
 The default implementation of this member function frees temporary objects and unused dynamic link libraries from memory.  
  
 This member function is used only in user-interface threads.  
  
 Because the application cannot process messages until `OnIdle` returns, do not perform lengthy tasks in this function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnIdle](../vs140/CWinApp--OnIdle.md)