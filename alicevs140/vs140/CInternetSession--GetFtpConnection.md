---
title: "CInternetSession::GetFtpConnection"
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
ms.assetid: 18565e06-ab74-4c19-a836-6a924ad17003
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::GetFtpConnection
Call this member function to establish an FTP connection and get a pointer to a `CFtpConnection` object.  
  
## Syntax  
  
```  
  
      CFtpConnection* GetFtpConnection(  
   LPCTSTR pstrServer,  
   LPCTSTR pstrUserName = NULL,  
   LPCTSTR pstrPassword = NULL,  
   INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,  
   BOOL bPassive = FALSE   
);  
```  
  
#### Parameters  
 `pstrServer`  
 A pointer to a string containing the FTP server name.  
  
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
  
 `nPort`  
 A number that identifies the TCP/IP port to use on the server.  
  
 `bPassive`  
 Specifies passive or active mode for this FTP session. If set to **TRUE**, it sets the Win32 API `dwFlag` to **INTERNET_FLAG_PASSIVE**.  
  
## Return Value  
 A pointer to a [CFtpConnection](../vs140/CFtpConnection-Class.md) object. If the call fails, determine the cause of the failure by examining the thrown [CInternetException](../vs140/CInternetException-Class.md) object.  
  
## Remarks  
 `GetFtpConnection` connects to an FTP server, and creates and returns a pointer to a **CFTPConnection** object. It does not perform any specific operation on the server. If you intend to read or write to files, for example, you must perform those operations as separate steps. See the classes [CFtpConnection](../vs140/CFtpConnection-Class.md) and [CFtpFileFind](../vs140/CFtpFileFind-Class.md) for information about searching for files, opening files, and reading or writing to files. See the article [Internet Programming with WinInet](../vs140/Win32-Internet-Extensions--WinInet-.md) for steps in performing common FTP connection tasks.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Example  
 See the example for [CFtpFileFind](../vs140/CFtpFileFind-Class.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [CInternetSession::GetGopherConnection](../vs140/CInternetSession--GetGopherConnection.md)   
 [CInternetSession::GetHttpConnection](../vs140/CInternetSession--GetHttpConnection.md)   
 [CInternetSession::OpenURL](../vs140/CInternetSession--OpenURL.md)