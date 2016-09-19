---
title: "CAsyncSocket::Listen"
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
ms.assetid: 644fcc6e-d25b-4a4b-be44-5223726449e3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::Listen
Call this member function to listen for incoming connection requests.  
  
## Syntax  
  
```  
  
      BOOL Listen(  
   int nConnectionBacklog = 5   
);  
```  
  
#### Parameters  
 *nConnectionBacklog*  
 The maximum length to which the queue of pending connections can grow. Valid range is from 1 to 5.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0, and a specific error code can be retrieved by calling [GetLastError](../vs140/CAsyncSocket--GetLastError.md). The following errors apply to this member function:  
  
-   **WSANOTINITIALISED** A successful [AfxSocketInit](../vs140/AfxSocketInit.md) must occur before using this API.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
-   **WSAEADDRINUSE** An attempt has been made to listen on an address in use.  
  
-   **WSAEINPROGRESS** A blocking Windows Sockets operation is in progress.  
  
-   **WSAEINVAL** The socket has not been bound with **Bind** or is already connected.  
  
-   **WSAEISCONN** The socket is already connected.  
  
-   **WSAEMFILE** No more file descriptors are available.  
  
-   `WSAENOBUFS` No buffer space is available.  
  
-   **WSAENOTSOCK** The descriptor is not a socket.  
  
-   **WSAEOPNOTSUPP** The referenced socket is not of a type that supports the `Listen` operation.  
  
## Remarks  
 To accept connections, the socket is first created with **Create**, a backlog for incoming connections is specified with `Listen`, and then the connections are accepted with **Accept**. `Listen` applies only to sockets that support connections, that is, those of type **SOCK_STREAM**. This socket is put into "passive" mode where incoming connections are acknowledged and queued pending acceptance by the process.  
  
 This function is typically used by servers (or any application that wants to accept connections) that could have more than one connection request at a time: if a connection request arrives with the queue full, the client will receive an error with an indication of **WSAECONNREFUSED**.  
  
 `Listen` attempts to continue to function rationally when there are no available ports (descriptors). It will accept connections until the queue is emptied. If ports become available, a later call to `Listen` or **Accept** will refill the queue to the current or most recent "backlog," if possible, and resume listening for incoming connections.  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Accept](../vs140/CAsyncSocket--Accept.md)   
 [CAsyncSocket::Connect](../vs140/CAsyncSocket--Connect.md)   
 [CAsyncSocket::Create](../vs140/CAsyncSocket--Create.md)