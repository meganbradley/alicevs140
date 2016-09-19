---
title: "Steps in a Typical Gopher Client Application"
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
ms.assetid: 3e4e1869-5da0-453d-8ba9-b648c894bb90
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Steps in a Typical Gopher Client Application
The following table shows the steps you might perform in a typical gopher client application.  
  
|Your goal|Actions you take|Effects|  
|---------------|----------------------|-------------|  
|Begin a gopher session.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) object.|Initializes WinInet and connects to server.|  
|Connect to a gopher server.|Use [CInternetSession::GetGopherConnection](../vs140/CInternetSession--GetGopherConnection.md).|Returns a [CGopherConnection](../vs140/CGopherConnection-Class.md) object.|  
|Find the first resource in the gopher.|Use [CGopherFileFind::FindFile](../vs140/CGopherFileFind--FindFile.md).|Finds the first file. Returns FALSE if no files are found.|  
|Find the next resource in the gopher.|Use [CGopherFileFind::FindNextFile](../vs140/CGopherFileFind--FindNextFile.md).|Finds the next file. Returns FALSE if the file is not found.|  
|Open the file found by **FindFile** or `FindNextFile` for reading.|Get a gopher locator using [CGopherFileFind::GetLocator](../vs140/CGopherFileFind--GetLocator.md). Use [CGopherConnection::OpenFile](../vs140/CGopherConnection--OpenFile.md).|Opens the file specified by the locator. `OpenFile` returns a [CGopherFile](../vs140/CGopherFile-Class.md) object.|  
|Open a file using a gopher locator you supply.|Create a gopher locator using [CGopherConnection::CreateLocator](../vs140/CGopherConnection--CreateLocator.md). Use [CGopherConnection::OpenFile](../vs140/CGopherConnection--OpenFile.md).|Opens the file specified by the locator. `OpenFile` returns a [CGopherFile](../vs140/CGopherFile-Class.md) object.|  
|Read from the file.|Use [CGopherFile](../vs140/CGopherFile-Class.md).|Reads the specified number of bytes, using a buffer you supply.|  
|Handle exceptions.|Use the [CInternetException](../vs140/CInternetException-Class.md) class.|Handles all common Internet exception types.|  
|End the gopher session.|Dispose of the [CInternetSession](../vs140/CInternetSession-Class.md) object.|Automatically cleans up open file handles and connections.|  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [Prerequisites for Internet Client Classes](../vs140/Prerequisites-for-Internet-Client-Classes.md)   
 [Writing an Internet Client Application Using MFC WinInet Classes](../vs140/Writing-an-Internet-Client-Application-Using-MFC-WinInet-Classes.md)