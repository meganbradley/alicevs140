---
title: "Steps in a Typical FTP Client Application"
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
ms.topic: article
ms.assetid: 70bed7b5-6040-40d1-bc77-702e63a698f2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Steps in a Typical FTP Client Application
A typical FTP client application creates a [CInternetSession](../vs140/CInternetSession-Class.md) and a [CFtpConnection](../vs140/CFtpConnection-Class.md) object. Note that these MFC WinInet classes do not actually control the proxy type settings; IIS does.  
  
 Also, see these Knowledge Base articles:  
  
-   HOWTO: FTP with CERN-Based Proxy Using WinInet API (Article ID: Q166961)  
  
-   SAMPLE: FTP with CERN-Based Password Protected Proxy (Article ID: Q216214)  
  
-   Internet Services Manager Fails to Show Installed Proxy Services (Article ID: Q216802)  
  
 The following table shows the steps you might perform in a typical FTP client application.  
  
|Your goal|Actions you take|Effects|  
|---------------|----------------------|-------------|  
|Begin an FTP session.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) object.|Initializes WinInet and connects to server.|  
|Connect to an FTP server.|Use [CInternetSession::GetFtpConnection](../vs140/CInternetSession--GetFtpConnection.md).|Returns a [CFtpConnection](../vs140/CFtpConnection-Class.md) object.|  
|Change to a new FTP directory on the server.|Use [CFtpConnection::SetCurrentDirectory](../vs140/CFtpConnection--SetCurrentDirectory.md).|Changes the directory you are currently connected to on the server.|  
|Find the first file in the FTP directory.|Use [CFtpFileFind::FindFile](../vs140/CFtpFileFind--FindFile.md).|Finds the first file. Returns FALSE if no files are found.|  
|Find the next file in the FTP directory.|Use [CFtpFileFind::FindNextFile](../vs140/CFtpFileFind--FindNextFile.md).|Finds the next file. Returns FALSE if the file is not found.|  
|Open the file found by **FindFile** or `FindNextFile` for reading or writing.|Use [CFtpConnection::OpenFile](../vs140/CFtpConnection--OpenFile.md), using the file name returned by [FindFile](../vs140/CFtpFileFind--FindFile.md) or [FindNextFile](../vs140/CFtpFileFind--FindNextFile.md).|Opens the file on the server for reading or writing. Returns a [CInternetFile](../vs140/CInternetFile-Class.md) object.|  
|Read from or write to the file.|Use [CInternetFile::Read](../vs140/CInternetFile--Read.md) or [CInternetFile::Write](../vs140/CInternetFile--Write.md).|Reads or writes the specified number of bytes, using a buffer you supply.|  
|Handle exceptions.|Use the [CInternetException](../vs140/CInternetException-Class.md) class.|Handles all common Internet exception types.|  
|End the FTP session.|Dispose of the [CInternetSession](../vs140/CInternetSession-Class.md) object.|Automatically cleans up open file handles and connections.|  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [Prerequisites for Internet Client Classes](../vs140/Prerequisites-for-Internet-Client-Classes.md)   
 [Writing an Internet Client Application Using MFC WinInet Classes](../vs140/Writing-an-Internet-Client-Application-Using-MFC-WinInet-Classes.md)