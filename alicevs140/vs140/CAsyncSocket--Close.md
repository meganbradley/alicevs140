---
title: "CAsyncSocket::Close"
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
ms.assetid: 41a847bd-1e7b-4edb-97e3-64f1df7adf1b
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::Close
Closes the socket.  
  
## Syntax  
  
```  
  
virtual void Close( );  
```  
  
## Remarks  
 This function releases the socket descriptor so that further references to it will fail with the error **WSAENOTSOCK**. If this is the last reference to the underlying socket, the associated naming information and queued data are discarded. The socket object's destructor calls **Close** for you.  
  
 For `CAsyncSocket`, but not for `CSocket`, the semantics of **Close** are affected by the socket options **SO_LINGER** and **SO_DONTLINGER**. For further information, see member function `GetSockOpt`.  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAsyncSocket::Accept](../vs140/CAsyncSocket--Accept.md)   
 [CAsyncSocket::CAsyncSocket](../vs140/CAsyncSocket--CAsyncSocket.md)   
 [CAsyncSocket::IOCtl](../vs140/CAsyncSocket--IOCtl.md)   
 [CAsyncSocket::GetSockOpt](../vs140/CAsyncSocket--GetSockOpt.md)   
 [CAsyncSocket::SetSockOpt](../vs140/CAsyncSocket--SetSockOpt.md)   
 [CAsyncSocket::AsyncSelect](../vs140/CAsyncSocket--AsyncSelect.md)