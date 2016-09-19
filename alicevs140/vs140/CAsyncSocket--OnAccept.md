---
title: "CAsyncSocket::OnAccept"
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
ms.assetid: 4272a1bf-4cc9-4246-8e46-d3398ea15fca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::OnAccept
Called by the framework to notify a listening socket that it can accept pending connection requests by calling the [Accept](../vs140/CAsyncSocket--Accept.md) member function.  
  
## Syntax  
  
```  
  
      virtual void OnAccept(  
   int nErrorCode   
);  
```  
  
#### Parameters  
 `nErrorCode`  
 The most recent error on a socket. The following error codes applies to the `OnAccept` member function:  
  
-   **0** The function executed successfully.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
## Remarks  
 For more information, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Accept](../vs140/CAsyncSocket--Accept.md)   
 [CAsyncSocket::GetLastError](../vs140/CAsyncSocket--GetLastError.md)   
 [CAsyncSocket::OnClose](../vs140/CAsyncSocket--OnClose.md)   
 [CAsyncSocket::OnConnect](../vs140/CAsyncSocket--OnConnect.md)   
 [CAsyncSocket::OnOutOfBandData](../vs140/CAsyncSocket--OnOutOfBandData.md)   
 [CAsyncSocket::OnReceive](../vs140/CAsyncSocket--OnReceive.md)   
 [CAsyncSocket::OnSend](../vs140/CAsyncSocket--OnSend.md)