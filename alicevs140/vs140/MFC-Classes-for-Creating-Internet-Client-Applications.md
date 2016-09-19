---
title: "MFC Classes for Creating Internet Client Applications"
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
ms.assetid: 67d34117-9839-4f4b-8bb8-0e4a9471c606
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MFC Classes for Creating Internet Client Applications
MFC provides the following classes and global functions for writing Internet client applications. Indentation indicates a class is derived from the unindented class above it. `CGopherFile` and `CHttpFile` derive from `CInternetFile`, for example. These classes and global functions are declared in AFXINET.H, except `CFileFind`, which is declared in AFX.H.  
  
## Classes  
  
-   [CInternetSession](../vs140/CInternetSession-Class.md)  
  
-   [CInternetConnection](../vs140/CInternetConnection-Class.md)  
  
    -   [CFtpConnection](../vs140/CFtpConnection-Class.md)  
  
    -   [CGopherConnection](../vs140/CGopherConnection-Class.md)  
  
    -   [CHttpConnection](../vs140/CHttpConnection-Class.md)  
  
-   [CInternetFile](../vs140/CInternetFile-Class.md)  
  
    -   [CGopherFile](../vs140/CGopherFile-Class.md)  
  
    -   [CHttpFile](../vs140/CHttpFile-Class.md)  
  
-   [CFileFind](../vs140/CFileFind-Class.md)  
  
    -   [CFtpFileFind](../vs140/CFtpFileFind-Class.md)  
  
    -   [CGopherFileFind](../vs140/CGopherFileFind-Class.md)  
  
-   [CGopherLocator](../vs140/CGopherLocator-Class.md)  
  
-   [CInternetException](../vs140/CInternetException-Class.md)  
  
## Global Functions  
  
-   [AfxParseURL](../vs140/AfxParseURL.md)  
  
-   [AfxGetInternetHandleType](../vs140/AfxGetInternetHandleType.md)  
  
-   [AfxThrowInternetException](../vs140/AfxThrowInternetException.md)  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [Prerequisites for Internet Client Classes](../vs140/Prerequisites-for-Internet-Client-Classes.md)   
 [Writing an Internet Client Application Using MFC WinInet Classes](../vs140/Writing-an-Internet-Client-Application-Using-MFC-WinInet-Classes.md)