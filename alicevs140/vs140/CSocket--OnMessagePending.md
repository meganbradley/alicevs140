---
title: "CSocket::OnMessagePending"
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
ms.assetid: 715e6082-72a7-4d44-8c09-f028d8285288
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocket::OnMessagePending
Override this member function to look for particular messages from Windows and respond to them in your socket.  
  
## Syntax  
  
```  
  
virtual BOOL OnMessagePending( );  
```  
  
## Return Value  
 Nonzero if the message was handled; otherwise 0.  
  
## Remarks  
 This is an advanced overridable.  
  
 The framework calls `OnMessagePending` while the socket is pumping Windows messages to give you an opportunity to deal with messages of interest to your application. For examples of how you might use `OnMessagePending`, see the article [Windows Sockets: Deriving from Socket Classes](../vs140/Windows-Sockets--Deriving-from-Socket-Classes.md).  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CSocket Class](../vs140/CSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSocket::CancelBlockingCall](../vs140/CSocket--CancelBlockingCall.md)   
 [CSocket::IsBlocking](../vs140/CSocket--IsBlocking.md)