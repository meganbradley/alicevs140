---
title: "CAsyncSocket::GetPeerName"
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
ms.assetid: 9dd6ca6e-aed7-4dfe-b469-e356ba99612d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::GetPeerName
Call this member function to get the address of the peer socket to which this socket is connected.  
  
## Syntax  
  
```  
  
      BOOL GetPeerName(  
   CString& rPeerAddress,  
   UINT& rPeerPort   
);  
BOOL GetPeerName(  
   SOCKADDR* lpSockAddr,  
   int* lpSockAddrLen   
);  
```  
  
#### Parameters  
 `rPeerAddress`  
 Reference to a `CString` object that receives a dotted number IP address.  
  
 `rPeerPort`  
 Reference to a **UINT** that stores a port.  
  
 `lpSockAddr`  
 A pointer to the [SOCKADDR](../vs140/SOCKADDR-Structure.md) structure that receives the name of the peer socket.  
  
 `lpSockAddrLen`  
 A pointer to the length of the address in `lpSockAddr` in bytes. On return, the `lpSockAddrLen` argument contains the actual size of `lpSockAddr` returned in bytes.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0, and a specific error code can be retrieved by calling [GetLastError](../vs140/CAsyncSocket--GetLastError.md). The following errors apply to this member function:  
  
-   **WSANOTINITIALISED** A successful [AfxSocketInit](../vs140/AfxSocketInit.md) must occur before using this API.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
-   **WSAEFAULT** The `lpSockAddrLen` argument is not large enough.  
  
-   **WSAEINPROGRESS** A blocking Windows Sockets call is in progress.  
  
-   **WSAENOTCONN** The socket is not connected.  
  
-   **WSAENOTSOCK** The descriptor is not a socket.  
  
## Remarks  
 To handle IPv6 addresses, use [CAsyncSocket::GetPeerNameEx](../vs140/CAsyncSocket--GetPeerNameEx.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Bind](../vs140/CAsyncSocket--Bind.md)   
 [CAsyncSocket::Connect](../vs140/CAsyncSocket--Connect.md)   
 [CAsyncSocket::Create](../vs140/CAsyncSocket--Create.md)   
 [CAsyncSocket::GetSockName](../vs140/CAsyncSocket--GetSockName.md)