---
title: "CWnd::SendNotifyMessage"
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
ms.assetid: 4955765a-162a-42be-8f35-b398d701b5b8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SendNotifyMessage
Sends the specified message to the window.  
  
## Syntax  
  
```  
  
      BOOL SendNotifyMessage(  
   UINT message,  
   WPARAM wParam,  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `message`  
 Specifies the message to be sent.  
  
 `wParam`  
 Specifies additional message-dependent information.  
  
 `lParam`  
 Specifies additional message-dependent information.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 If the window was created by the calling thread, `SendNotifyMessage` calls the window procedure for the window and does not return until the window procedure has processed the message. If the window was created by a different thread, `SendNotifyMessage` passes the message to the window procedure and returns immediately; it does not wait for the window procedure to finish processing the message.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SendMessage](../vs140/CWnd--SendMessage.md)   
 [SendNotifyMessage](http://msdn.microsoft.com/library/windows/desktop/ms644953)