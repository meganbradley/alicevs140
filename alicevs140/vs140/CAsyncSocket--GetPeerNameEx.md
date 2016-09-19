---
title: "CAsyncSocket::GetPeerNameEx"
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
ms.assetid: 0b145607-487c-4f6a-90c9-66afe48f8ad4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::GetPeerNameEx
Call this member function to get the address of the peer socket to which this socket is connected (handles IPv6 addresses).  
  
## Syntax  
  
```  
  
      BOOL GetPeerNameEx(  
   CString& rPeerAddress,  
   UINT& rPeerPort   
);  
```  
  
#### Parameters  
 `rPeerAddress`  
 Reference to a `CString` object that receives a dotted number IP address.  
  
 `rPeerPort`  
 Reference to a **UINT** that stores a port.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0, and a specific error code can be retrieved by calling [GetLastError](../vs140/CAsyncSocket--GetLastError.md). The following errors apply to this member function:  
  
-   **WSANOTINITIALISED** A successful [AfxSocketInit](../vs140/AfxSocketInit.md) must occur before using this API.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
-   **WSAEFAULT** The `lpSockAddrLen` argument is not large enough.  
  
-   **WSAEINPROGRESS** A blocking Windows Sockets call is in progress.  
  
-   **WSAENOTCONN** The socket is not connected.  
  
-   **WSAENOTSOCK** The descriptor is not a socket.  
  
## Remarks  
 This function is the same as [CAsyncSocket::GetPeerName](../vs140/CAsyncSocket--GetPeerName.md) except that it handles IPv6 addresses as well as older protocols.  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Bind](../vs140/CAsyncSocket--Bind.md)   
 [CAsyncSocket::Connect](../vs140/CAsyncSocket--Connect.md)   
 [CAsyncSocket::Create](../vs140/CAsyncSocket--Create.md)   
 [CAsyncSocket::GetSockName](../vs140/CAsyncSocket--GetSockName.md)