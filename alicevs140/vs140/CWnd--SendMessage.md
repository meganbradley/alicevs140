---
title: "CWnd::SendMessage"
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
ms.assetid: ba72b0bd-57ec-4ef5-bee4-f5dbb971f927
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::SendMessage
Sends the specified message to this window.  
  
## Syntax  
  
```  
  
      LRESULT SendMessage(  
   UINT message,  
   WPARAM wParam = 0,  
   LPARAM lParam = 0   
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
 The result of the message processing; its value depends on the message sent.  
  
## Remarks  
 The **SendMessage** member function calls the window procedure directly and does not return until that window procedure has processed the message. This is in contrast to the [PostMessage](../vs140/CWnd--PostMessage.md) member function, which places the message into the window's message queue and returns immediately.  
  
## Example  
 [!CODE [NVC_MFCWindowing#101](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#101)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [InSendMessage](http://msdn.microsoft.com/library/windows/desktop/ms644941)   
 [CWnd::PostMessage](../vs140/CWnd--PostMessage.md)   
 [CWnd::SendDlgItemMessage](../vs140/CWnd--SendDlgItemMessage.md)   
 [SendMessage](http://msdn.microsoft.com/library/windows/desktop/ms644950)