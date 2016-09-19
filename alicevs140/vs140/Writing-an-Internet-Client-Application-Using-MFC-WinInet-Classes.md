---
title: "Writing an Internet Client Application Using MFC WinInet Classes"
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
ms.assetid: a2c4a40c-a94e-4b3e-9dbf-f8a8dc8e5428
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Writing an Internet Client Application Using MFC WinInet Classes
The basis of every Internet client application is the Internet session. MFC implements Internet sessions as objects of class [CInternetSession](../vs140/CInternetSession-Class.md). Using this class, you can create one Internet session or several simultaneous sessions.  
  
 To communicate with a server, you need a [CInternetConnection](../vs140/CInternetConnection-Class.md) object as well as a `CInternetSession`. You can create a `CInternetConnection` by using [CInternetSession::GetFtpConnection](../vs140/CInternetSession--GetFtpConnection.md), [CInternetSession::GetHttpConnection](../vs140/CInternetSession--GetHttpConnection.md), or [CInternetSession::GetGopherConnection](../vs140/CInternetSession--GetGopherConnection.md). Each of these calls is specific to the protocol type. These calls do not open a file on the server for reading or writing. If you intend to read or write data, you must open the file as a separate step.  
  
 For most Internet sessions, the `CInternetSession` object works hand-in-hand with a [CInternetFile](../vs140/CInternetFile-Class.md) object:  
  
-   For an Internet session, you must create an instance of [CInternetSession](../vs140/CInternetSession-Class.md).  
  
-   If your Internet session reads or writes data, you must create an instance of `CInternetFile` (or its subclasses, [CHttpFile](../vs140/CHttpFile-Class.md) or [CGopherFile](../vs140/CGopherFile-Class.md)). The easiest way to read data is to call [CInternetSession::OpenURL](../vs140/CInternetSession--OpenURL.md). This function parses a Universal Resource Locator (URL) supplied by you, opens a connection to the server specified by the URL, and returns a read-only `CInternetFile` object. `CInternetSession::OpenURL` is not specific to one protocol type — the same call works for any FTP, HTTP, or gopher URL. `CInternetSession::OpenURL` even works with local files (returning a `CStdioFile` instead of a `CInternetFile`).  
  
-   If your Internet session does not read or write data, but performs other tasks, such as deleting a file in an FTP directory, you may not need to create an instance of `CInternetFile`.  
  
 There are two ways to create a `CInternetFile` object:  
  
-   If you use `CInternetSession::OpenURL` to establish your server connection, the call to `OpenURL` returns a `CStdioFile`.  
  
-   If use **CInternetSession::GetFtpConnection**, `GetGopherConnection`, or `GetHttpConnection` to establish your server connection, you must call `CFtpConnection::OpenFile`, `CGopherConnection::OpenFile`, or **CHttpConnection::OpenRequest,** respectively, to return a `CInternetFile`, `CGopherFile`, or `CHttpFile`, respectively.  
  
 The steps in implementing an Internet client application vary depending on whether you create a generic Internet client based on **OpenURL** or a protocol-specific client using one of the **GetConnection** functions.  
  
## What do you want to know more about?  
  
-   [How do I write an Internet client application that works generically with FTP, HTTP, and gopher?](../vs140/Steps-in-a-Typical-Internet-Client-Application.md)  
  
-   [How do I write an FTP client application that opens a file?](../vs140/Steps-in-a-Typical-FTP-Client-Application.md)  
  
-   [How do I write an FTP client application that does not open a file but performs a directory operation, such as deleting a file?](../vs140/Steps-in-a-Typical-FTP-Client-Application-to-Delete-a-File.md)  
  
-   [How do I write a gopher client application?](../vs140/Steps-in-a-Typical-Gopher-Client-Application.md)  
  
-   [How do I write an HTTP client application?](../vs140/Steps-in-a-Typical-HTTP-Client-Application.md)  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [MFC Classes for Creating Internet Client Applications](../vs140/MFC-Classes-for-Creating-Internet-Client-Applications.md)   
 [Prerequisites for Internet Client Classes](../vs140/Prerequisites-for-Internet-Client-Classes.md)