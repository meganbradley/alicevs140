---
title: "CFtpConnection::OpenFile"
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
ms.assetid: c40cdb6a-5c75-43cf-9c31-98a63ea40c97
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpConnection::OpenFile
Call this member function to open a file located on an FTP server for reading or writing.  
  
## Syntax  
  
```  
  
      CInternetFile* OpenFile(  
   LPCTSTR pstrFileName,  
   DWORD dwAccess = GENERIC_READ,  
   DWORD dwFlags = FTP_TRANSFER_TYPE_BINARY,  
   DWORD_PTR dwContext = 1   
);  
```  
  
#### Parameters  
 `pstrFileName`  
 A pointer to a string containing the name of the file to be opened.  
  
 *dwAccess*  
 Determines how the file will be accessed. Can be either GENERIC_READ or GENERIC_WRITE, but not both.  
  
 `dwFlags`  
 Specifies the conditions under which subsequent transfers occur. This can be any of the following FTP_TRANSFER_* constants:  
  
-   FTP_TRANSFER_TYPE_ASCII   The file transfers using FTP ASCII (Type A) transfer method. Converts control and formatting information to local equivalents.  
  
-   FTP_TRANSFER_TYPE_BINARY   The file transfers data using FTP's Image (Type I) transfer method. The file transfers data exactly as it exists, with no changes. This is the default transfer method.  
  
 `dwContext`  
 The context identifier for opening the file. See **Remarks** for more information about `dwContext`.  
  
## Return Value  
 A pointer to a [CInternetFile](../vs140/CInternetFile-Class.md) object.  
  
## Remarks  
 `OpenFile` should be used in the following situations:  
  
-   An application has data that needs to be sent and created as a file on the FTP server, but that data is not in a local file. Once `OpenFile` opens a file, the application uses [CInternetFile::Write](../vs140/CInternetFile--Write.md) to send the FTP file data to the server.  
  
-   An application must retrieve a file from the server and place it into application-controlled memory, instead of writing it to disk. The application uses [CInternetFile::Read](../vs140/CInternetFile--Read.md) after using `OpenFile` to open the file.  
  
-   An application needs a fine level of control over a file transfer. For example, the application may want to display a progress control indicate the progress of the file transfer status while downloading a file.  
  
 After calling `OpenFile` and until calling **CInternetConnection::Close**, the application can only call [CInternetFile::Read](../vs140/CInternetFile--Read.md), [CInternetFile::Write](../vs140/CInternetFile--Write.md), **CInternetConnection::Close**, or [CFtpFileFind::FindFile](../vs140/CFtpFileFind--FindFile.md). Calls to other FTP functions for the same FTP session will fail and set the error code to FTP_ETRANSFER_IN_PROGRESS.  
  
 The `pstrFileName` parameter can be either a partially qualified filename relative to the current directory or fully qualified. A backslash (\\) or forward slash (/) can be used as the directory separator for either name. `OpenFile` translates the directory name separators to the appropriate characters before using it.  
  
 Override the `dwContext` default to set the context identifier to a value of your choosing. The context identifier is associated with this specific operation of the `CFtpConnection` object created by its [CInternetSession](../vs140/CInternetSession-Class.md) object. The value is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to provide status on the operation with which it is identified. See the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)   
 [CFtpConnection::GetFile](../vs140/CFtpConnection--GetFile.md)   
 [CGopherConnection::OpenFile](../vs140/CGopherConnection--OpenFile.md)   
 [CInternetFile::Write](../vs140/CInternetFile--Write.md)   
 [CInternetFile::Read](../vs140/CInternetFile--Read.md)