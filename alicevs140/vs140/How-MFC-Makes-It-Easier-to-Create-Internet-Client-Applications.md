---
title: "How MFC Makes It Easier to Create Internet Client Applications"
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
ms.assetid: 94437b3f-f15c-437d-b5fd-264a2efec9ab
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How MFC Makes It Easier to Create Internet Client Applications
The Microsoft Foundation Classes encapsulate the Win32 Internet Extension (WinInet) functions in a manner that provides a familiar context for MFC programmers. MFC provides three Internet file classes ([CInternetFile](../vs140/CInternetFile-Class.md), [CHttpFile](../vs140/CHttpFile-Class.md), and [CGopherFile](../vs140/CGopherFile-Class.md)) derived from the [CStdioFile](../vs140/CStdioFile-Class.md) class. Not only do these classes make retrieving and manipulating Internet data familiar to programmers who have used `CStdioFile` for local files, but with these classes you can handle local files and Internet files in a consistent, transparent manner.  
  
 The MFC WinInet classes provide the same functionality as `CStdioFile` for data that is transferred across the Internet. These classes abstract the Internet protocols for HTTP, FTP, and gopher into a high-level application programming interface, providing a fast and straightforward path to making applications Internet-aware. For example, connecting to an FTP server still requires several steps at a low level, but as an MFC developer, you only need to make one call to `CInternetSession::GetFTPConnection` to create that connection.  
  
 In addition, the MFC WinInet classes provide the following advantages:  
  
-   Buffered I/O  
  
-   Type-safe handles for your data  
  
-   Default parameters for many functions  
  
-   Exception handling for common Internet errors  
  
-   Automatic cleanup of open handles and connections  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [How WinInet Makes It Easier to Create Internet Client Applications](../vs140/How-WinInet-Makes-It-Easier-to-Create-Internet-Client-Applications.md)