---
title: "CWindow::SendNotifyMessage"
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
ms.assetid: c14931f2-4669-473c-b05d-f6e0b3c07a45
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::SendNotifyMessage
Sends a message to the window.  
  
## Syntax  
  
```  
  
      BOOL SendNotifyMessage(  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0   
) throw();  
```  
  
## Remarks  
 See [SendNotifyMessage](http://msdn.microsoft.com/library/windows/desktop/ms644953) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 If the window was created by the calling thread, `SendNotifyMessage` does not return until the window procedure has processed the message. Otherwise, it returns immediately.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::SendMessage](../vs140/CWindow--SendMessage.md)   
 [CWindow::SendMessageToDescendants](../vs140/CWindow--SendMessageToDescendants.md)   
 [CWindow::PostMessage](../vs140/CWindow--PostMessage.md)