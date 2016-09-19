---
title: "CInternetSession::GetHttpConnection"
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
ms.assetid: b54a4477-315e-42bc-af49-1bcbd412e0a5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::GetHttpConnection
Call this member function to establish an HTTP connection and get a pointer to a `CHttpConnection` object.  
  
## Syntax  
  
```  
  
      CHttpConnection* GetHttpConnection(  
   LPCTSTR pstrServer,  
   INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,  
   LPCTSTR pstrUserName = NULL,  
   LPCTSTR pstrPassword = NULL   
);  
CHttpConnection* GetHttpConnection(  
   LPCTSTR pstrServer,  
   DWORD dwFlags,  
   INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,  
   LPCTSTR pstrUserName = NULL,  
   LPCTSTR pstrPassword = NULL   
);  
```  
  
#### Parameters  
 `pstrServer`  
 A pointer to a string containing the HTTP server name.  
  
 `nPort`  
 A number that identifies the TCP/IP port to use on the server.  
  
 `pstrUserName`  
 A pointer to a string containing the user name.  
  
 `pstrPassword`  
 A pointer to a string containing the access password.  
  
 *dwflags*  
 Any combination of the **INTERNET_ FLAG_\*** flags. See the table in the **Remarks** section of [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md) for a description of `dwFlags` values.  
  
## Return Value  
 A pointer to a [CHttpConnection](../vs140/CHttpConnection-Class.md) object. If the call fails, determine the cause of the failure by examining the thrown [CInternetException](../vs140/CInternetException-Class.md) object.  
  
## Remarks  
 `GetHttpConnection` connects to an HTTP server, and creates and returns a pointer to a `CHttpConnection` object. It does not perform any specific operation on the server. If you intend to query an HTTP header, for example, you must perform this operation as a separate step. See the classes [CHttpConnection](../vs140/CHttpConnection-Class.md) and [CHttpFile](../vs140/CHttpFile-Class.md) for information about operations you can perform by using a connection to an HTTP server. For information about browsing an HTTP site, see the member function [OpenURL](../vs140/CInternetSession--OpenURL.md). See the article [Internet Programming with WinInet](../vs140/Win32-Internet-Extensions--WinInet-.md) for steps in performing common HTTP connection tasks.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHttpConnection Class](../vs140/CHttpConnection-Class.md)   
 [CInternetSession::GetGopherConnection](../vs140/CInternetSession--GetGopherConnection.md)   
 [CInternetSession::GetFtpConnection](../vs140/CInternetSession--GetFtpConnection.md)   
 [CInternetSession::OpenURL](../vs140/CInternetSession--OpenURL.md)