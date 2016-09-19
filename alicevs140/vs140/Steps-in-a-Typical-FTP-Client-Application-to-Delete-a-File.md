---
title: "Steps in a Typical FTP Client Application to Delete a File"
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
ms.assetid: 2c347a96-c0a4-4827-98fe-668406e552bc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Steps in a Typical FTP Client Application to Delete a File
The following table shows the steps you might perform in a typical FTP client application that deletes a file.  
  
|Your goal|Actions you take|Effects|  
|---------------|----------------------|-------------|  
|Begin an FTP session.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) object.|Initializes WinInet and connects to server.|  
|Connect to an FTP server.|Use [CInternetSession::GetFtpConnection](../vs140/CInternetSession--GetFtpConnection.md).|Returns a [CFtpConnection](../vs140/CFtpConnection-Class.md) object.|  
|Check to make sure you're in the right directory on the FTP server.|Use [CFtpConnection::GetCurrentDirectory](../vs140/CFtpConnection--GetCurrentDirectory.md) or [CFtpConnection::GetCurrentDirectoryAsURL](../vs140/CFtpConnection--GetCurrentDirectoryAsURL.md).|Returns the name or URL of the directory you are currently connected to on the server, depending on the member function selected.|  
|Change to a new FTP directory on the server.|Use [CFtpConnection::SetCurrentDirectory](../vs140/CFtpConnection--SetCurrentDirectory.md).|Changes the directory you are currently connected to on the server.|  
|Find the first file in the FTP directory.|Use [CFtpFileFind::FindFile](../vs140/CFtpFileFind--FindFile.md).|Finds the first file. Returns FALSE if no files are found.|  
|Find the next file in the FTP directory.|Use [CFtpFileFind::FindNextFile](../vs140/CFtpFileFind--FindNextFile.md).|Finds the next file. Returns FALSE if the file is not found.|  
|Delete the file found by **FindFile** or `FindNextFile`.|Use [CFtpConnection::Remove](../vs140/CFtpConnection--Remove.md), using the file name returned by **FindFile** or `FindNextFile`.|Deletes the file on the server for reading or writing.|  
|Handle exceptions.|Use the [CInternetException](../vs140/CInternetException-Class.md) class.|Handles all common Internet exception types.|  
|End the FTP session.|Dispose of the [CInternetSession](../vs140/CInternetSession-Class.md) object.|Automatically cleans up open file handles and connections.|  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [Prerequisites for Internet Client Classes](../vs140/Prerequisites-for-Internet-Client-Classes.md)   
 [Writing an Internet Client Application Using MFC WinInet Classes](../vs140/Writing-an-Internet-Client-Application-Using-MFC-WinInet-Classes.md)