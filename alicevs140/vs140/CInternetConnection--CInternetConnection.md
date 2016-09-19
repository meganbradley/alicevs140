---
title: "CInternetConnection::CInternetConnection"
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
ms.assetid: 22aca50b-9ea5-4d8a-8d51-3253867e3679
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetConnection::CInternetConnection
This member function is called when a `CInternetConnection` object is created.  
  
## Syntax  
  
```  
  
      CInternetConnection(  
   CInternetSession* pSession,  
   LPCTSTR pstrServer,  
   INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,  
   DWORD_PTR dwContext = 1   
);  
```  
  
#### Parameters  
 `pSession`  
 A pointer to a [CInternetSession](../vs140/CInternetSession-Class.md) object.  
  
 `pstrServer`  
 A pointer to a string containing the server name.  
  
 `nPort`  
 The number that identifies the Internet port for this connection.  
  
 `dwContext`  
 The context identifier for the `CInternetConnection` object. See **Remarks** for more information about `dwContext`.  
  
## Remarks  
 You never call `CInternetConnection` yourself; instead, call the [CInternetSession](../vs140/CInternetSession-Class.md) member function for the type of connection you want to establish:  
  
-   [CInternetSession::GetFtpConnection](../vs140/CInternetSession--GetFtpConnection.md)  
  
-   [CInternetSession::GetHttpConnection](../vs140/CInternetSession--GetHttpConnection.md)  
  
-   [CInternetSession::GetGopherConnection](../vs140/CInternetSession--GetGopherConnection.md)  
  
 The default value for `dwContext` is sent by MFC to the `CInternetConnection`-derived object from the [CInternetSession](../vs140/CInternetSession-Class.md) object that created the **InternetConnection**-derived object. The default is set to 1; however, you can explicitly assign a specific context identifier in the [CInternetSession](../vs140/CInternetSession--CInternetSession.md) constructor for the connection. The object and any work it does will be associated with that context ID. The context identifier is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to provide status on the object with which it is identified. See the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)   
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [CHttpConnection Class](../vs140/CHttpConnection-Class.md)