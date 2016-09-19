---
title: "CSocket::CancelBlockingCall"
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
ms.assetid: 9805ac6a-ac98-4e6f-99c0-6c28797c4e9a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocket::CancelBlockingCall
Call this member function to cancel a blocking call currently in progress.  
  
## Syntax  
  
```  
  
void CancelBlockingCall( );  
```  
  
## Remarks  
 This function cancels any outstanding blocking operation for this socket. The original blocking call will terminate as soon as possible with the error **WSAEINTR**.  
  
 In the case of a blocking **Connect** operation, the Windows Sockets implementation will terminate the blocking call as soon as possible, but it may not be possible for the socket resources to be released until the connection has completed (and then been reset) or timed out. This is likely to be noticeable only if the application immediately tries to open a new socket (if no sockets are available), or to connect to the same peer.  
  
 Canceling any operation other than **Accept** can leave the socket in an indeterminate state. If an application cancels a blocking operation on a socket, the only operation that the application can depend on being able to perform on the socket is a call to **Close**, although other operations may work on some Windows Sockets implementations. If you desire maximum portability for your application, you must be careful not to depend on performing operations after a cancel.  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CSocket Class](../vs140/CSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Accept](../vs140/CAsyncSocket--Accept.md)   
 [CAsyncSocket::Close](../vs140/CAsyncSocket--Close.md)   
 [CAsyncSocket::Connect](../vs140/CAsyncSocket--Connect.md)   
 [CSocket::IsBlocking](../vs140/CSocket--IsBlocking.md)   
 [WSASetBlockingHook](http://msdn.microsoft.com/library/windows/desktop/ms742205)