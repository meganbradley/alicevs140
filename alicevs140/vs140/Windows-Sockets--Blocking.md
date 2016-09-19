---
title: "Windows Sockets: Blocking"
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
ms.assetid: 10aca9b1-bfba-41a8-9c55-ea8082181e63
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Windows Sockets: Blocking
This article and two companion articles explain several issues in Windows Sockets programming. This article covers blocking. The other issues are covered in the articles: [Windows Sockets: Byte Ordering](../vs140/Windows-Sockets--Byte-Ordering.md) and [Windows Sockets: Converting Strings](../vs140/Windows-Sockets--Converting-Strings.md).  
  
 If you use or derive from class [CAsyncSocket](../vs140/CAsyncSocket-Class.md), you will need to manage these issues yourself. If you use or derive from class [CSocket](../vs140/CSocket-Class.md), MFC manages them for you.  
  
## Blocking  
 A socket can be in "blocking mode" or "nonblocking mode." The functions of sockets in blocking (or synchronous) mode do not return until they can complete their action. This is called blocking because the socket whose function was called cannot do anything — is blocked — until the call returns. A call to the **Receive** member function, for example, might take an arbitrarily long time to complete as it waits for the sending application to send (this is if you are using `CSocket`, or using `CAsyncSocket` with blocking). If a `CAsyncSocket` object is in nonblocking mode (operating asynchronously), the call returns immediately and the current error code, retrievable with the [GetLastError](../vs140/CAsyncSocket--GetLastError.md) member function, is **WSAEWOULDBLOCK**, indicating that the call would have blocked had it not returned immediately because of the mode. (`CSocket` never returns **WSAEWOULDBLOCK**. The class manages blocking for you.)  
  
 The behavior of sockets is different under 32-bit and 64-bit operating systems (such as Windows 95 or Windows 98) than under 16-bit operating systems (such as Windows 3.1). Unlike 16-bit operating systems, the 32-bit and 64-bit operating systems use preemptive multitasking and provide multithreading. Under the 32-bit and 64-bit operating systems, you can put your sockets in separate worker threads. A socket in a thread can block without interfering with other activities in your application and without spending compute time on the blocking. For information on multithreaded programming, see the article [Multithreading](../vs140/Multithreading-Support-for-Older-Code--Visual-C---.md).  
  
> [!NOTE]
>  In multithreaded applications, you can use the blocking nature of `CSocket` to simplify your program's design without affecting the responsiveness of the user interface. By handling user interactions in the main thread and `CSocket` processing in alternate threads, you can separate these logical operations. In an application that is not multithreaded, these two activities must be combined and handled as a single thread, which usually means using `CAsyncSocket` so you can handle communications requests on demand, or overriding `CSocket::OnMessagePending` to handle user actions during lengthy synchronous activity.  
  
 The rest of this discussion is for programmers targeting 16-bit operating systems:  
  
 Normally, if you are using `CAsyncSocket`, you should avoid using blocking operations and operate asynchronously instead. In asynchronous operations, from the point at which you receive a **WSAEWOULDBLOCK** error code after calling **Receive**, for example, you wait until your `OnReceive` member function is called to notify you that you can read again. Asynchronous calls are made by calling back your socket's appropriate callback notification function, such as [OnReceive](../vs140/CAsyncSocket--OnReceive.md).  
  
 Under Windows, blocking calls are considered bad practice. By default, [CAsyncSocket](../vs140/CAsyncSocket-Class.md) supports asynchronous calls, and you must manage the blocking yourself using callback notifications. Class [CSocket](../vs140/CSocket-Class.md), on the other hand, is synchronous. It pumps Windows messages and manages blocking for you.  
  
 For more information about blocking, see the Windows Sockets specification. For more information about "On" functions, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md) and [Windows Sockets: Deriving from Socket Classes](../vs140/Windows-Sockets--Deriving-from-Socket-Classes.md).  
  
 For more information, see:  
  
-   [Windows Sockets: Using Class CAsyncSocket](../vs140/Windows-Sockets--Using-Class-CAsyncSocket.md)  
  
-   [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md)  
  
-   [Windows Sockets: Background](../vs140/Windows-Sockets--Background.md)  
  
-   [Windows Sockets: Stream Sockets](../vs140/Windows-Sockets--Stream-Sockets.md)  
  
-   [Windows Sockets: Datagram Sockets](../vs140/Windows-Sockets--Datagram-Sockets.md)  
  
## See Also  
 [Windows Sockets in MFC](../vs140/Windows-Sockets-in-MFC.md)   
 [CAsyncSocket::OnSend](../vs140/CAsyncSocket--OnSend.md)