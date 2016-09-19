---
title: "CAsyncSocket::OnOutOfBandData"
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
ms.assetid: 410c2ce7-cb1e-42cb-8437-917fec7e6ca2
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::OnOutOfBandData
Called by the framework to notify the receiving socket that the sending socket has out-of-band data to send.  
  
## Syntax  
  
```  
  
      virtual void OnOutOfBandData(  
   int nErrorCode   
);  
```  
  
#### Parameters  
 `nErrorCode`  
 The most recent error on a socket. The following error codes apply to the `OnOutOfBandData` member function:  
  
-   **0** The function executed successfully.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
## Remarks  
 Out-of-band data is a logically independent channel that is associated with each pair of connected sockets of type **SOCK_STREAM**. The channel is generally used to send urgent data.  
  
 MFC supports out-of-band data, but users of class `CAsyncSocket` are discouraged from using it. The easier way is to create a second socket for passing such data. For more information about out-of-band data, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::GetLastError](../vs140/CAsyncSocket--GetLastError.md)   
 [CAsyncSocket::OnAccept](../vs140/CAsyncSocket--OnAccept.md)   
 [CAsyncSocket::OnClose](../vs140/CAsyncSocket--OnClose.md)   
 [CAsyncSocket::OnConnect](../vs140/CAsyncSocket--OnConnect.md)   
 [CAsyncSocket::OnReceive](../vs140/CAsyncSocket--OnReceive.md)   
 [CAsyncSocket::OnSend](../vs140/CAsyncSocket--OnSend.md)