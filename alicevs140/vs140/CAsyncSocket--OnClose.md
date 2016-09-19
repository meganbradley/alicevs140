---
title: "CAsyncSocket::OnClose"
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
ms.assetid: 941a2eec-a428-468e-a33e-d8a2603c2cb2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::OnClose
Called by the framework to notify this socket that the connected socket is closed by its process.  
  
## Syntax  
  
```  
  
      virtual void OnClose(  
   int nErrorCode   
);  
```  
  
#### Parameters  
 `nErrorCode`  
 The most recent error on a socket. The following error codes apply to the `OnClose` member function:  
  
-   **0** The function executed successfully.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
-   **WSAECONNRESET** The connection was reset by the remote side.  
  
-   **WSAECONNABORTED** The connection was aborted due to timeout or other failure.  
  
## Remarks  
 For more information, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Close](../vs140/CAsyncSocket--Close.md)   
 [CAsyncSocket::GetLastError](../vs140/CAsyncSocket--GetLastError.md)   
 [CAsyncSocket::OnAccept](../vs140/CAsyncSocket--OnAccept.md)   
 [CAsyncSocket::OnConnect](../vs140/CAsyncSocket--OnConnect.md)   
 [CAsyncSocket::OnOutOfBandData](../vs140/CAsyncSocket--OnOutOfBandData.md)   
 [CAsyncSocket::OnReceive](../vs140/CAsyncSocket--OnReceive.md)   
 [CAsyncSocket::OnSend](../vs140/CAsyncSocket--OnSend.md)