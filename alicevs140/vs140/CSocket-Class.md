---
title: "CSocket Class"
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
ms.assetid: 7f23c081-d24d-42e3-b511-8053ca53d729
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSocket Class
Derives from `CAsyncSocket`, inherits its encapsulation of the Windows Sockets API, and represents a higher level of abstraction than that of a `CAsyncSocket` object.  
  
## Syntax  
  
```  
class CSocket : public CAsyncSocket  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSocket::CSocket](#csocket__csocket)|Constructs a `CSocket` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSocket::Attach](#csocket__attach)|Attaches a **SOCKET** handle to a `CSocket` object.|  
|[CSocket::CancelBlockingCall](#csocket__cancelblockingcall)|Cancels a blocking call that is currently in progress.|  
|[CSocket::Create](#csocket__create)|Creates a socket.|  
|[CSocket::FromHandle](#csocket__fromhandle)|Returns a pointer to a `CSocket` object, given a **SOCKET** handle.|  
|[CSocket::IsBlocking](#csocket__isblocking)|Determines whether a blocking call is in progress.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSocket::OnMessagePending](#csocket__onmessagepending)|Called to process pending messages while waiting for a blocking call to complete.|  
  
## Remarks  
 `CSocket` works with classes `CSocketFile` and `CArchive` to manage the sending and receiving of data.  
  
 A `CSocket` object also provides blocking, which is essential to the synchronous operation of `CArchive`. Blocking functions, such as `Receive`, `Send`, `ReceiveFrom`, `SendTo`, and `Accept` (all inherited from `CAsyncSocket`), do not return a `WSAEWOULDBLOCK` error in `CSocket`. Instead, these functions wait until the operation completes. Additionally, the original call will terminate with the error `WSAEINTR` if `CancelBlockingCall` is called while one of these functions is blocking.  
  
 To use a `CSocket` object, call the constructor, then call `Create` to create the underlying `SOCKET` handle (type `SOCKET`). The default parameters of `Create` create a stream socket, but if you are not using the socket with a `CArchive` object, you can specify a parameter to create a datagram socket instead, or bind to a specific port to create a server socket. Connect to a client socket using `Connect` on the client side and `Accept` on the server side. Then create a `CSocketFile` object and associate it to the `CSocket` object in the `CSocketFile` constructor. Next, create a `CArchive` object for sending and one for receiving data (as needed), then associate them with the `CSocketFile` object in the `CArchive` constructor. When communications are complete, destroy the `CArchive`, `CSocketFile`, and `CSocket` objects. The `SOCKET` data type is described in the article [Windows Sockets: Background](../vs140/Windows-Sockets--Background.md).  
  
 When you use `CArchive` with `CSocketFile` and `CSocket`, you might encounter a situation where `CSocket::Receive` enters a loop (by `PumpMessages(FD_READ)`) waiting for the requested amount of bytes. This is because Windows sockets allow only one recv call per FD_READ notification, but `CSocketFile` and `CSocket` allow multiple recv calls per FD_READ. If you get an FD_READ when there is no data to read, the application hangs. If you never get another FD_READ, the application stops communicating over the socket.  
  
 You can resolve this problem as follows. In the `OnReceive` method of your socket class, call `CAsyncSocket::IOCtl(FIONREAD, ...)` before you call the `Serialize` method of your message class when the expected data to be read from the socket exceeds the size of one TCP packet (maximum transmission unit of the network medium, usually at least 1096 bytes). If the size of the available data is less than needed, wait for all the data to be received and only then start the read operation.  
  
 In the following example, `m_dwExpected` is the approximate number of bytes that the user expects to receive. It is assumed that you declare it elsewhere in your code.  
  
 [!CODE [NVC_MFCSocketThread#4](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSocketThread#4)]  
  
> [!NOTE]
>  When using MFC sockets in secondary threads in a statically linked MFC application, you must call `AfxSocketInit` in each thread that uses sockets to initialize the socket libraries. By default, `AfxSocketInit` is called only in the primary thread.  
  
 For more information, see [Windows Sockets in MFC](../vs140/Windows-Sockets-in-MFC.md), [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md), [Windows Sockets: How Sockets with Archives Work](../vs140/Windows-Sockets--How-Sockets-with-Archives-Work.md), [Windows Sockets: Sequence of Operations](../vs140/Windows-Sockets--Sequence-of-Operations.md), [Windows Sockets: Example of Sockets Using Archives](../vs140/Windows-Sockets--Example-of-Sockets-Using-Archives.md).  
  
## Inheritance Hierarchy  
 [CObject](../vs140/CObject-Class.md)  
  
 [CAsyncSocket](../vs140/CAsyncSocket-Class.md)  
  
 `CSocket`  
  
## Requirements  
 **Header:** afxsock.h  
  
##  <a name="csocket__attach"></a>  CSocket::Attach  
 Call this member function to attach the `hSocket` handle to a `CSocket` object.  
  
```  
BOOL Attach(    SOCKET hSocket );  
  
```  
  
### Parameters  
 `hSocket`  
 Contains a handle to a socket.  
  
### Return Value  
 Nonzero if the function is successful.  
  
### Remarks  
 The **SOCKET** handle is stored in the object's [m_hSocket](../vs140/CAsyncSocket-Class.md#casyncsocket__m_hsocket) data member.  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
### Example  
 [!CODE [NVC_MFCSocketThread#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSocketThread#1)]  
  
 [!CODE [NVC_MFCSocketThread#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSocketThread#2)]  
  
 [!CODE [NVC_MFCSocketThread#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSocketThread#3)]  
  
##  <a name="csocket__cancelblockingcall"></a>  CSocket::CancelBlockingCall  
 Call this member function to cancel a blocking call currently in progress.  
  
```  
void CancelBlockingCall( );  
```  
  
### Remarks  
 This function cancels any outstanding blocking operation for this socket. The original blocking call will terminate as soon as possible with the error **WSAEINTR**.  
  
 In the case of a blocking **Connect** operation, the Windows Sockets implementation will terminate the blocking call as soon as possible, but it may not be possible for the socket resources to be released until the connection has completed (and then been reset) or timed out. This is likely to be noticeable only if the application immediately tries to open a new socket (if no sockets are available), or to connect to the same peer.  
  
 Canceling any operation other than **Accept** can leave the socket in an indeterminate state. If an application cancels a blocking operation on a socket, the only operation that the application can depend on being able to perform on the socket is a call to **Close**, although other operations may work on some Windows Sockets implementations. If you desire maximum portability for your application, you must be careful not to depend on performing operations after a cancel.  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
##  <a name="csocket__create"></a>  CSocket::Create  
 Call the **Create** member function after constructing a socket object to create the Windows socket and attach it.  
  
```  
BOOL Create(    UINT nSocketPort = 0,    int nSocketType = SOCK_STREAM,    LPCTSTR lpszSocketAddress = NULL );  
  
```  
  
### Parameters  
 `nSocketPort`  
 A particular port to be used with the socket, or 0 if you want MFC to select a port.  
  
 `nSocketType`  
 **SOCK_STREAM** or **SOCK_DGRAM**.  
  
 `lpszSocketAddress`  
 A pointer to a string containing the network address of the connected socket, a dotted number such as "128.56.22.8". Passing the **NULL** string for this parameter indicates the **CSocket** instance should listen for client activity on all network interfaces.  
  
### Return Value  
 Nonzero if the function is successful; otherwise 0, and a specific error code can be retrieved by calling `GetLastError`.  
  
### Remarks  
 **Create** then calls **Bind** to bind the socket to the specified address. The following socket types are supported:  
  
-   **SOCK_STREAM** Provides sequenced, reliable, two-way, connection-based byte streams. Uses Transmission Control Protocol (TCP) for the Internet address family.  
  
-   **SOCK_DGRAM** Supports datagrams, which are connectionless, unreliable buffers of a fixed (typically small) maximum length. Uses User Datagram Protocol (UDP) for the Internet address family. To use this option, you must not use the socket with a `CArchive` object.  
  
    > [!NOTE]
    >  The **Accept** member function takes a reference to a new, empty `CSocket` object as its parameter. You must construct this object before you call **Accept**. Keep in mind that if this socket object goes out of scope, the connection closes. Do not call **Create** for this new socket object.  
  
 For more information about stream and datagram sockets, see the articles [Windows Sockets: Background](../vs140/Windows-Sockets--Background.md), [Windows Sockets: Ports and Socket Addresses](../vs140/Windows-Sockets--Ports-and-Socket-Addresses.md), and [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
##  <a name="csocket__csocket"></a>  CSocket::CSocket  
 Constructs a `CSocket` object.  
  
```  
CSocket( );  
  
```  
  
### Remarks  
 After construction, you must call the **Create** member function.  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
##  <a name="csocket__fromhandle"></a>  CSocket::FromHandle  
 Returns a pointer to a `CSocket` object.  
  
```  
static CSocket* PASCAL FromHandle(    SOCKET hSocket );  
  
```  
  
### Parameters  
 `hSocket`  
 Contains a handle to a socket.  
  
### Return Value  
 A pointer to a `CSocket` object, or **NULL** if there is no `CSocket` object attached to `hSocket`.  
  
### Remarks  
 When given a **SOCKET** handle, if a `CSocket` object is not attached to the handle, the member function returns **NULL** and does not create a temporary object.  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
##  <a name="csocket__isblocking"></a>  CSocket::IsBlocking  
 Call this member function to determine if a blocking call is in progress.  
  
```  
BOOL IsBlocking( );  
  
```  
  
### Return Value  
 Nonzero if the socket is blocking; otherwise 0.  
  
### Remarks  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
##  <a name="csocket__onmessagepending"></a>  CSocket::OnMessagePending  
 Override this member function to look for particular messages from Windows and respond to them in your socket.  
  
```  
virtual BOOL OnMessagePending( );  
  
```  
  
### Return Value  
 Nonzero if the message was handled; otherwise 0.  
  
### Remarks  
 This is an advanced overridable.  
  
 The framework calls `OnMessagePending` while the socket is pumping Windows messages to give you an opportunity to deal with messages of interest to your application. For examples of how you might use `OnMessagePending`, see the article [Windows Sockets: Deriving from Socket Classes](../vs140/Windows-Sockets--Deriving-from-Socket-Classes.md).  
  
 For more information, see [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md).  
  
## See Also  
 [Base Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket](../vs140/CAsyncSocket-Class.md)   
 [CSocketFile](../vs140/CSocketFile-Class.md)