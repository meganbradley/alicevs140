---
title: "CAsyncSocket::OnReceive"
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
ms.assetid: 4a056dd8-8987-4476-b394-6e298313606c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::OnReceive
Called by the framework to notify this socket that there is data in the buffer that can be retrieved by calling the **Receive** member function.  
  
## Syntax  
  
```  
  
      virtual void OnReceive(  
   int nErrorCode   
);  
```  
  
#### Parameters  
 `nErrorCode`  
 The most recent error on a socket. The following error codes apply to the `OnReceive` member function:  
  
-   **0** The function executed successfully.  
  
-   **WSAENETDOWN** The Windows Sockets implementation detected that the network subsystem failed.  
  
## Remarks  
 For more information, see [Windows Sockets: Socket Notifications](../vs140/Windows-Sockets--Socket-Notifications.md).  
  
## Example  
 [!CODE [NVC_MFCAsyncSocket#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAsyncSocket#2)]  
  
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
 [CAsyncSocket::OnSend](../vs140/CAsyncSocket--OnSend.md)   
 [CAsyncSocket::Receive](../vs140/CAsyncSocket--Receive.md)