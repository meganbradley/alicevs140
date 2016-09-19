---
title: "CAsyncSocket::AsyncSelect"
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
ms.assetid: 4713f26e-621c-47bd-a140-e3886d141cbd
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::AsyncSelect
Call this member function to request event notification for a socket.  
  
## Syntax  
  
```  
  
      BOOL AsyncSelect(  
   long lEvent = FD_READ | FD_WRITE | FD_OOB | FD_ACCEPT | FD_CONNECT | FD_CLOSE   
);  
```  
  
#### Parameters  
 `lEvent`  
 A bitmask which specifies a combination of network events in which the application is interested.  
  
-   **FD_READ** Want to receive notification of readiness for reading.  
  
-   **FD_WRITE** Want to receive notification when data is available to be read.  
  
-   **FD_OOB** Want to receive notification of the arrival of out-of-band data.  
  
-   **FD_ACCEPT** Want to receive notification of incoming connections.  
  
-   **FD_CONNECT** Want to receive notification of connection results.  
  
-   **FD_CLOSE** Want to receive notification when a socket has been closed by a peer.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0, and a specific error code can be retrieved by calling [GetLastError](../vs140/CAsyncSocket--GetLastError.md). The following errors apply to this member function:  
  
-   **WSANOTINITIALISED** A successful [AfxSocketInit](../vs140/AfxSocketInit.md) must occur before using this API.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
-   **WSAEINVAL** Indicates that one of the specified parameters was invalid.  
  
-   **WSAEINPROGRESS** A blocking Windows Sockets operation is in progress.  
  
## Remarks  
 This function is used to specify which MFC callback notification functions will be called for the socket. `AsyncSelect` automatically sets this socket to nonblocking mode. For more information, see the article [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::GetLastError](../vs140/CAsyncSocket--GetLastError.md)   
 [WSAAsyncSelect](http://msdn.microsoft.com/library/windows/desktop/ms741540)