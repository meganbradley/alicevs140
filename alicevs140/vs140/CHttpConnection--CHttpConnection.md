---
title: "CHttpConnection::CHttpConnection"
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
ms.assetid: b4479392-9707-42b7-8581-5b18be90cc76
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpConnection::CHttpConnection
This member function is called to construct a `CHttpConnection` object.  
  
## Syntax  
  
```  
  
      CHttpConnection(   
   CInternetSession* pSession,   
   HINTERNET hConnected,   
   LPCTSTR pstrServer,   
   DWORD_PTR dwContext   
);  
CHttpConnection(   
   CInternetSession* pSession,   
   LPCTSTR pstrServer,   
   INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,   
   LPCTSTR pstrUserName = NULL,   
   LPCTSTR pstrPassword = NULL,   
   DWORD_PTR dwContext = 1   
);  
CHttpConnection(   
   CInternetSession* pSession,   
   LPCTSTR pstrServer,   
   DWORD dwFlags,   
   INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,   
   LPCTSTR pstrUserName = NULL,   
   LPCTSTR pstrPassword = NULL,   
   DWORD_PTR dwContext = 1   
);  
```  
  
#### Parameters  
 `pSession`  
 A pointer to a [CInternetSession](../vs140/CInternetSession-Class.md) object.  
  
 `hConnected`  
 A handle to an Internet connection.  
  
 `pstrServer`  
 A pointer to a string containing the server name.  
  
 `dwContext`  
 The context identifier for the `CInternetConnection` object. See **Remarks** for more information about `dwContext`.  
  
 `nPort`  
 The number that identifies the Internet port for this connection.  
  
 `pstrUserName`  
 Pointer to a null-terminated string that specifies the name of the user to log in. If **NULL**, the default is anonymous.  
  
 `pstrPassword`  
 A pointer to a null-terminated string that specifies the password to use to log in. If both `pstrPassword` and `pstrUserName` are **NULL**, the default anonymous password is the user's email name. If `pstrPassword` is **NULL** (or an empty string) but `pstrUserName` is not **NULL**, a blank password is used. The following table describes the behavior for the four possible settings of `pstrUserName` and `pstrPassword`:  
  
|`pstrUserName`|`pstrPassword`|Username sent to FTP server|Password sent to FTP server|  
|--------------------|--------------------|---------------------------------|---------------------------------|  
|**NULL** or " "|**NULL** or " "|"anonymous"|User's email name|  
|Non-**NULL** String|**NULL** or " "|`pstrUserName`|" "|  
|**NULL** Non-**NULL** String|**ERROR**|**ERROR**||  
|Non-**NULL** String|Non-**NULL** String|`pstrUserName`|`pstrPassword`|  
  
 `dwFlags`  
 Any combination of the **INTERNET_ FLAG_\*** flags. See the table in the **Remarks** section of [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md) for a description of `dwFlags` values.  
  
## Remarks  
 You never create a `CHttpConnection` directly. Rather, you create an object by calling [CInternetSession::GetHttpConnection](../vs140/CInternetSession--GetHttpConnection.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpConnection Class](../vs140/CHttpConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetSession::GetHttpConnection](../vs140/CInternetSession--GetHttpConnection.md)   
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)