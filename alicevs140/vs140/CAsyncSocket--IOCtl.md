---
title: "CAsyncSocket::IOCtl"
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
ms.assetid: a8c6c380-d874-49db-ba7c-f5e560a2fe1d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::IOCtl
Call this member function to control the mode of a socket.  
  
## Syntax  
  
```  
  
      BOOL IOCtl(  
   long lCommand,  
   DWORD* lpArgument   
);  
```  
  
#### Parameters  
 `lCommand`  
 The command to perform on the socket.  
  
 `lpArgument`  
 A pointer to a parameter for `lCommand`.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0, and a specific error code can be retrieved by calling [GetLastError](../vs140/CAsyncSocket--GetLastError.md). The following errors apply to this member function:  
  
-   **WSANOTINITIALISED** A successful [AfxSocketInit](../vs140/AfxSocketInit.md) must occur before using this API.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
-   **WSAEINVAL** `lCommand` is not a valid command, or `lpArgument` is not an acceptable parameter for `lCommand`, or the command is not applicable to the type of socket supplied.  
  
-   **WSAEINPROGRESS** A blocking Windows Sockets operation is in progress.  
  
-   **WSAENOTSOCK** The descriptor is not a socket.  
  
## Remarks  
 This routine can be used on any socket in any state. It is used to get or retrieve operating parameters associated with the socket, independent of the protocol and communications subsystem. The following commands are supported:  
  
-   **FIONBIO** Enable or disable nonblocking mode on the socket. The `lpArgument` parameter points at a `DWORD`, which is nonzero if nonblocking mode is to be enabled and zero if it is to be disabled. If `AsyncSelect` has been issued on a socket, then any attempt to use **IOCtl** to set the socket back to blocking mode will fail with **WSAEINVAL**. To set the socket back to blocking mode and prevent the **WSAEINVAL** error, an application must first disable `AsyncSelect` by calling `AsyncSelect` with the `lEvent` parameter equal to 0, then call **IOCtl**.  
  
-   **FIONREAD** Determine the maximum number of bytes that can be read with one **Receive** call from this socket. The `lpArgument` parameter points at a `DWORD` in which **IOCtl** stores the result. If this socket is of type **SOCK_STREAM**, **FIONREAD** returns the total amount of data which can be read in a single **Receive**; this is normally the same as the total amount of data queued on the socket. If this socket is of type **SOCK_DGRAM**, **FIONREAD** returns the size of the first datagram queued on the socket.  
  
-   **SIOCATMARK** Determine whether all out-of-band data has been read. This applies only to a socket of type **SOCK_STREAM** which has been configured for in-line reception of any out-of-band data (**SO_OOBINLINE**). If no out-of-band data is waiting to be read, the operation returns nonzero. Otherwise it returns 0, and the next **Receive** or `ReceiveFrom` performed on the socket will retrieve some or all of the data preceding the "mark"; the application should use the **SIOCATMARK** operation to determine whether any data remains. If there is any normal data preceding the "urgent" (out-of-band) data, it will be received in order. (Note that a **Receive** or `ReceiveFrom` will never mix out-of-band and normal data in the same call.) The `lpArgument` parameter points at a `DWORD` in which **IOCtl** stores the result.  
  
 This function is a subset of **ioctl()** as used in Berkeley sockets. In particular, there is no command which is equivalent to **FIOASYNC**, while **SIOCATMARK** is the only socket-level command which is supported.  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::AsyncSelect](../vs140/CAsyncSocket--AsyncSelect.md)   
 [CAsyncSocket::Create](../vs140/CAsyncSocket--Create.md)   
 [CAsyncSocket::GetSockOpt](../vs140/CAsyncSocket--GetSockOpt.md)   
 [CAsyncSocket::SetSockOpt](../vs140/CAsyncSocket--SetSockOpt.md)