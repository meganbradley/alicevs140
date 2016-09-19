---
title: "Windows Sockets in MFC"
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
ms.topic: article
ms.assetid: 1f3c476a-9c68-49fe-9a25-d22971a334d0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Windows Sockets in MFC
> [!NOTE]
>  MFC supports Windows Sockets 1 but does not support [Windows Sockets 2](http://msdn.microsoft.com/library/windows/desktop/ms740673). Windows Sockets 2 first shipped with Windows 98 and is the version included with Windows 2000.  
  
 MFC supplies two models for writing network communications programs with Windows Sockets, embodied in two MFC classes. This article describes these models and further details MFC sockets support. A "socket" is an endpoint of communication: an object through which your application communicates with other Windows Sockets applications across a network.  
  
 For information on Windows Sockets, including an explanation of the socket concept, see [Windows Sockets: Background](../vs140/Windows-Sockets--Background.md).  
  
##  <a name="_core_sockets_programming_models"></a> Sockets Programming Models  
 The two MFC Windows Sockets programming models are supported by the following classes:  
  
-   `CAsyncSocket`  
  
     This class encapsulates the Windows Sockets API. [CAsyncSocket](../vs140/CAsyncSocket-Class.md) is for programmers who know network programming and want the flexibility of programming directly to the sockets API but also want the convenience of callback functions for notification of network events. Other than packaging sockets in object-oriented form for use in C++, the only additional abstraction this class supplies is converting certain socket-related Windows messages into callbacks. For more information, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
-   `CSocket`  
  
     This class, derived from `CAsyncSocket`, supplies a higher level abstraction for working with sockets through an MFC [CArchive](../vs140/CArchive-Class.md) object. Using a socket with an archive greatly resembles using MFC's file serialization protocol. This makes it easier to use than the `CAsyncSocket` model. [CSocket](../vs140/CSocket-Class.md) inherits many member functions from `CAsyncSocket` that encapsulate Windows Sockets APIs; you will have to use some of these functions and understand sockets programming generally. But `CSocket` manages many aspects of the communication that you would have to do yourself using either the raw API or class `CAsyncSocket`. Most importantly, `CSocket` provides blocking (with background processing of Windows messages), which is essential to the synchronous operation of `CArchive`.  
  
 Creating and using `CSocket` and `CAsyncSocket` objects is described in [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md) and [Windows Sockets: Using Class CAsyncSocket](../vs140/Windows-Sockets--Using-Class-CAsyncSocket.md).  
  
##  <a name="_core_mfc_socket_samples_and_windows_sockets_dlls"></a> Windows Sockets DLLs  
 The Microsoft Windows operating systems supply the Windows Sockets dynamic-link libraries (DLL). Visual C++ supplies the appropriate header files and libraries and the Windows Sockets specification.  
  
> [!NOTE]
>  Under Windows NT and Windows 2000, Windows Sockets support for 16-bit applications is based on WINSOCK.DLL. For 32-bit applications, the support is in WSOCK32.DLL. The APIs provided are identical except that the 32-bit versions have parameters widened to 32 bits. Under Win32, thread safety is supplied.  
  
 For more information about Windows Sockets, see:  
  
-   [Windows Sockets: Stream Sockets](../vs140/Windows-Sockets--Stream-Sockets.md)  
  
-   [Windows Sockets: Datagram Sockets](../vs140/Windows-Sockets--Datagram-Sockets.md)  
  
-   [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md)  
  
-   [Windows Sockets: Sequence of Operations](../vs140/Windows-Sockets--Sequence-of-Operations.md)  
  
-   [Windows Sockets: Example of Sockets Using Archives](../vs140/Windows-Sockets--Example-of-Sockets-Using-Archives.md)  
  
-   [Windows Sockets: How Sockets with Archives Work](../vs140/Windows-Sockets--How-Sockets-with-Archives-Work.md)  
  
-   [Windows Sockets: Using Class CAsyncSocket](../vs140/Windows-Sockets--Using-Class-CAsyncSocket.md)  
  
-   [Windows Sockets: Deriving from Socket Classes](../vs140/Windows-Sockets--Deriving-from-Socket-Classes.md)  
  
-   [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md)  
  
-   [Windows Sockets: Blocking](../vs140/Windows-Sockets--Blocking.md)  
  
-   [Windows Sockets: Byte Ordering](../vs140/Windows-Sockets--Byte-Ordering.md)  
  
-   [Windows Sockets: Converting Strings](../vs140/Windows-Sockets--Converting-Strings.md)  
  
-   [Windows Sockets: Ports and Socket Addresses](../vs140/Windows-Sockets--Ports-and-Socket-Addresses.md)  
  
## See Also  
 [Windows Sockets](../vs140/Windows-Sockets.md)