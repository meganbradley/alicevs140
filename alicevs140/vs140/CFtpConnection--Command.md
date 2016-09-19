---
title: "CFtpConnection::Command"
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
ms.assetid: da4bef1d-7a31-4fc3-8ef2-8ff793becd68
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpConnection::Command
Sends a command directly to an FTP server.  
  
## Syntax  
  
```  
  
      CInternetFile* Command(  
   LPCTSTR pszCommand,  
   CmdResponseType eResponse = CmdRespNone,  
   DWORD dwFlags = FTP_TRANSFER_TYPE_BINARY,  
   DWORD_PTR dwContext = 1   
);  
```  
  
#### Parameters  
 `pszCommand`  
 A pointer to a string containing the command to be sent.  
  
 *eResponse*  
 Determines whether a response is expected from the FTP server. Can be one of the following values:  
  
-   **CmdRespNone** No response is expected.  
  
-   **CmdRespRead** A response is expected.  
  
 `dwFlags`  
 A value containing the flags that control this function. For a complete list, see [FTPCommand](http://msdn.microsoft.com/library/windows/desktop/aa384133).  
  
 `dwContext`  
 A pointer to a value containing an application-defined value used to identify the application context in callbacks.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function emulates the functionality of the [FTPCommand](http://msdn.microsoft.com/library/windows/desktop/aa384133) function, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 If an error occurs, MFC throws an exception of type [CInternetException](../vs140/CInternetException-Class.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)