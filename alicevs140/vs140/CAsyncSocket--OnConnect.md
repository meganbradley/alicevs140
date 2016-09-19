---
title: "CAsyncSocket::OnConnect"
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
ms.assetid: b20a26af-d80f-4dad-b720-3c1cac59d0c0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::OnConnect
Called by the framework to notify this connecting socket that its connection attempt is completed, whether successfully or in error.  
  
## Syntax  
  
```  
  
      virtual void OnConnect(  
   int nErrorCode   
);  
```  
  
#### Parameters  
 `nErrorCode`  
 The most recent error on a socket. The following error codes apply to the `OnConnect` member function:  
  
-   **0** The function executed successfully.  
  
-   **WSAEADDRINUSE** The specified address is already in use.  
  
-   **WSAEADDRNOTAVAIL** The specified address is not available from the local machine.  
  
-   **WSAEAFNOSUPPORT** Addresses in the specified family cannot be used with this socket.  
  
-   **WSAECONNREFUSED** The attempt to connect was forcefully rejected.  
  
-   **WSAEDESTADDRREQ** A destination address is required.  
  
-   **WSAEFAULT** The `lpSockAddrLen` argument is incorrect.  
  
-   **WSAEINVAL** The socket is already bound to an address.  
  
-   **WSAEISCONN** The socket is already connected.  
  
-   **WSAEMFILE** No more file descriptors are available.  
  
-   **WSAENETUNREACH** The network cannot be reached from this host at this time.  
  
-   `WSAENOBUFS` No buffer space is available. The socket cannot be connected.  
  
-   **WSAENOTCONN** The socket is not connected.  
  
-   **WSAENOTSOCK** The descriptor is a file, not a socket.  
  
-   **WSAETIMEDOUT** The attempt to connect timed out without establishing a connection.  
  
## Remarks  
  
> [!NOTE]
>  In [CSocket](../vs140/CSocket-Class.md), the `OnConnect` notification function is never called. For connections, you simply call **Connect**, which will return when the connection is completed (either successfully or in error). How connection notifications are handled is an MFC implementation detail.  
  
 For more information, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
## Example  
 [!CODE [NVC_MFCAsyncSocket#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAsyncSocket#1)]  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Connect](../vs140/CAsyncSocket--Connect.md)   
 [CAsyncSocket::GetLastError](../vs140/CAsyncSocket--GetLastError.md)   
 [CAsyncSocket::OnAccept](../vs140/CAsyncSocket--OnAccept.md)   
 [CAsyncSocket::OnClose](../vs140/CAsyncSocket--OnClose.md)   
 [CAsyncSocket::OnOutOfBandData](../vs140/CAsyncSocket--OnOutOfBandData.md)   
 [CAsyncSocket::OnReceive](../vs140/CAsyncSocket--OnReceive.md)   
 [CAsyncSocket::OnSend](../vs140/CAsyncSocket--OnSend.md)