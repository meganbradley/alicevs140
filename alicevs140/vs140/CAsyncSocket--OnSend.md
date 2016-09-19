---
title: "CAsyncSocket::OnSend"
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
ms.assetid: d2d3fa87-30e2-4dd2-852e-2d509ac93b90
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::OnSend
Called by the framework to notify the socket that it can now send data by calling the **Send** member function.  
  
## Syntax  
  
```  
  
      virtual void OnSend(  
   int nErrorCode   
);  
```  
  
#### Parameters  
 `nErrorCode`  
 The most recent error on a socket. The following error codes apply to the `OnSend` member function:  
  
-   **0** The function executed successfully.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
## Remarks  
 For more information, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
## Example  
 [!CODE [NVC_MFCAsyncSocket#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAsyncSocket#3)]  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::GetLastError](../vs140/CAsyncSocket--GetLastError.md)   
 [CAsyncSocket::OnAccept](../vs140/CAsyncSocket--OnAccept.md)   
 [CAsyncSocket::OnClose](../vs140/CAsyncSocket--OnClose.md)   
 [CAsyncSocket::OnConnect](../vs140/CAsyncSocket--OnConnect.md)   
 [CAsyncSocket::OnOutOfBandData](../vs140/CAsyncSocket--OnOutOfBandData.md)   
 [CAsyncSocket::OnReceive](../vs140/CAsyncSocket--OnReceive.md)   
 [CAsyncSocket::Send](../vs140/CAsyncSocket--Send.md)