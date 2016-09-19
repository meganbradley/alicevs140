---
title: "Prerequisites for Internet Client Classes"
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
ms.assetid: c51d1dfe-260c-4228-8100-e4efd90e9599
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Prerequisites for Internet Client Classes
Some actions taken by an Internet client (reading a file, for example) have prerequisite actions (in this case, establishing an Internet connection). The following tables list the prerequisites for some client actions.  
  
### General Internet URL (FTP, Gopher, or HTTP)  
  
|Action|Prerequisite|  
|------------|------------------|  
|Establish a connection.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) to establish the basis of an Internet client application.|  
|Open a URL.|Establish a connection. Call [CInternetSession::OpenURL](../vs140/CInternetSession--OpenURL.md). The `OpenURL` function returns a read-only resource object.|  
|Read URL data.|Open the URL. Call [CInternetFile::Read](../vs140/CInternetFile--Read.md).|  
|Set an Internet option.|Establish a connection. Call [CInternetSession::SetOption](../vs140/CInternetSession--SetOption.md).|  
|Set a function to be called with status information.|Establish a connection. Call [CInternetSession::EnableStatusCallback](../vs140/CInternetSession--EnableStatusCallback.md). Override [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to handle calls.|  
  
### FTP  
  
|Action|Prerequisite|  
|------------|------------------|  
|Establish an FTP connection.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) as the basis of this Internet client application. Call [CInternetSession::GetFtpConnection](../vs140/CInternetSession--GetFtpConnection.md) to create a [CFtpConnection](../vs140/CFtpConnection-Class.md) object.|  
|Find the first resource.|Establish an FTP connection. Create a [CFtpFileFind](../vs140/CFtpFileFind-Class.md) object. Call [CFtpFileFind::FindFile](../vs140/CFtpFileFind--FindFile.md).|  
|Enumerate all available resources.|Find the first file. Call [CFtpFileFind::FindNextFile](../vs140/CFtpFileFind--FindNextFile.md) until it returns FALSE.|  
|Open an FTP file.|Establish an FTP connection. Call [CFtpConnection::OpenFile](../vs140/CFtpConnection--OpenFile.md) to create and open a [CInternetFile](../vs140/CInternetFile-Class.md) object.|  
|Read an FTP file.|Open an FTP file with read access. Call [CInternetFile::Read](../vs140/CInternetFile--Read.md).|  
|Write to an FTP file.|Open an FTP file with write access. Call [CInternetFile::Write](../vs140/CInternetFile--Write.md).|  
|Change the client's directory on the server.|Establish an FTP connection. Call [CFtpConnection::SetCurrentDirectory](../vs140/CFtpConnection--SetCurrentDirectory.md).|  
|Retrieve the client's current directory on the server.|Establish an FTP connection. Call [CFtpConnection::GetCurrentDirectory](../vs140/CFtpConnection--GetCurrentDirectory.md).|  
  
### HTTP  
  
|Action|Prerequisite|  
|------------|------------------|  
|Establish an HTTP connection.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) as the basis of this Internet client application. Call [CInternetSession::GetHttpConnection](../vs140/CInternetSession--GetHttpConnection.md) to create a [CHttpConnection](../vs140/CHttpConnection-Class.md) object.|  
|Open an HTTP file.|Establish an HTTP connection. Call [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md) to create a [CHttpFile](../vs140/CHttpFile-Class.md) object. Call [CHttpFile::AddRequestHeaders](../vs140/CHttpFile--AddRequestHeaders.md). Call [CHttpFile::SendRequest](../vs140/CHttpFile--SendRequest.md).|  
|Read an HTTP file.|Open an HTTP file. Call [CInternetFile::Read](../vs140/CInternetFile--Read.md).|  
|Get information about an HTTP request.|Establish an HTTP connection. Call [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md) to create a [CHttpFile](../vs140/CHttpFile-Class.md) object. Call [CHttpFile::QueryInfo](../vs140/CHttpFile--QueryInfo.md).|  
  
### Gopher  
  
|Action|Prerequisite|  
|------------|------------------|  
|Establish a gopher connection.|Create a [CInternetSession](../vs140/CInternetSession-Class.md) as the basis of this Internet client application. Call [CInternetSession::GetGopherConnection](../vs140/CInternetSession--GetGopherConnection.md) to create a [CGopherConnection](../vs140/CGopherConnection-Class.md).|  
|Find the first file in the current directory.|Establish a gopher connection. Create a [CGopherFileFind](../vs140/CGopherFileFind-Class.md) object. Call [CGopherConnection::CreateLocator](../vs140/CGopherConnection--CreateLocator.md) to create a [CGopherLocator](../vs140/CGopherLocator-Class.md) object. Pass the locator to [CGopherFileFind::FindFile](../vs140/CGopherFileFind--FindFile.md). Call [CGopherFileFind::GetLocator](../vs140/CGopherFileFind--GetLocator.md) to get the locator of a file if you need it later.|  
|Enumerate all available files.|Find the first file. Call [CGopherFileFind::FindNextFile](../vs140/CGopherFileFind--FindNextFile.md) until it returns FALSE.|  
|Open a gopher file.|Establish a gopher connection. Create a gopher locator with [CGopherConnection::CreateLocator](../vs140/CGopherConnection--CreateLocator.md) or find a locator with [CGopherFileFind::GetLocator](../vs140/CGopherFileFind--GetLocator.md). Call [CGopherConnection::OpenFile](../vs140/CGopherConnection--OpenFile.md).|  
|Read a gopher file.|Open a gopher file. Use [CGopherFile](../vs140/CGopherFile-Class.md).|  
  
## See Also  
 [Win32 Internet Extensions (WinInet)](../vs140/Win32-Internet-Extensions--WinInet-.md)   
 [MFC Classes for Creating Internet Client Applications](../vs140/MFC-Classes-for-Creating-Internet-Client-Applications.md)   
 [Writing an Internet Client Application Using MFC WinInet Classes](../vs140/Writing-an-Internet-Client-Application-Using-MFC-WinInet-Classes.md)