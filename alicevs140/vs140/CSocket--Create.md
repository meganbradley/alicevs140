---
title: "CSocket::Create"
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
ms.assetid: 1f64e6da-ba77-43a5-9606-d7c65536a2b8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocket::Create
Call the **Create** member function after constructing a socket object to create the Windows socket and attach it.  
  
## Syntax  
  
```  
  
      BOOL Create(  
   UINT nSocketPort = 0,  
   int nSocketType = SOCK_STREAM,  
   LPCTSTR lpszSocketAddress = NULL   
);  
```  
  
#### Parameters  
 `nSocketPort`  
 A particular port to be used with the socket, or 0 if you want MFC to select a port.  
  
 `nSocketType`  
 **SOCK_STREAM** or **SOCK_DGRAM**.  
  
 `lpszSocketAddress`  
 A pointer to a string containing the network address of the connected socket, a dotted number such as "128.56.22.8". Passing the **NULL** string for this parameter indicates the **CSocket** instance should listen for client activity on all network interfaces.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0, and a specific error code can be retrieved by calling `GetLastError`.  
  
## Remarks  
 **Create** then calls **Bind** to bind the socket to the specified address. The following socket types are supported:  
  
-   **SOCK_STREAM** Provides sequenced, reliable, two-way, connection-based byte streams. Uses Transmission Control Protocol (TCP) for the Internet address family.  
  
-   **SOCK_DGRAM** Supports datagrams, which are connectionless, unreliable buffers of a fixed (typically small) maximum length. Uses User Datagram Protocol (UDP) for the Internet address family. To use this option, you must not use the socket with a `CArchive` object.  
  
    > [!NOTE]
    >  The **Accept** member function takes a reference to a new, empty `CSocket` object as its parameter. You must construct this object before you call **Accept**. Keep in mind that if this socket object goes out of scope, the connection closes. Do not call **Create** for this new socket object.  
  
 For more information about stream and datagram sockets, see the articles [Windows Sockets: Background](../vs140/Windows-Sockets--Background.md), [Windows Sockets: Ports and Socket Addresses](../vs140/Windows-Sockets--Ports-and-Socket-Addresses.md), and [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CSocket Class](../vs140/CSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Create](../vs140/CAsyncSocket--Create.md)   
 [CAsyncSocket::Bind](../vs140/CAsyncSocket--Bind.md)