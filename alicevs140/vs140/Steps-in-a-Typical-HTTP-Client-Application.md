---
title: "Steps in a Typical HTTP Client Application"
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
ms.assetid: f86552e8-8acd-4b23-bdc5-0c3a247ebd74
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Steps in a Typical HTTP Client Application
The following table shows the steps you might perform in a typical HTTP client application:  
  
|Your goal|Actions you take|Effects|  
|---------------|----------------------|-------------|  
|Begin an HTTP session.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) object.|Initializes WinInet and connects to server.|  
|Connect to an HTTP server.|Use [CInternetSession::GetHttpConnection](../vs140/CInternetSession--GetHttpConnection.md).|Returns a [CHttpConnection](../vs140/CHttpConnection-Class.md) object.|  
|Open an HTTP request.|Use [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md).|Returns a [CHttpFile](../vs140/CHttpFile-Class.md) object.|  
|Send an HTTP request.|Use [CHttpFile::AddRequestHeaders](../vs140/CHttpFile--AddRequestHeaders.md) and [CHttpFile::SendRequest](../vs140/CHttpFile--SendRequest.md).|Finds the file. Returns FALSE if the file is not found.|  
|Read from the file.|Use [CHttpFile](../vs140/CHttpFile-Class.md).|Reads the specified number of bytes using a buffer you supply.|  
|Handle exceptions.|Use the [CInternetException](../vs140/CInternetException-Class.md) class.|Handles all common Internet exception types.|  
|End the HTTP session.|Dispose of the [CInternetSession](../vs140/CInternetSession-Class.md) object.|Automatically cleans up open file handles and connections.|  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [Prerequisites for Internet Client Classes](../vs140/Prerequisites-for-Internet-Client-Classes.md)   
 [Writing an Internet Client Application Using MFC WinInet Classes](../vs140/Writing-an-Internet-Client-Application-Using-MFC-WinInet-Classes.md)