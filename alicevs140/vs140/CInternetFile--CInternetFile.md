---
title: "CInternetFile::CInternetFile"
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
ms.assetid: 89396a11-dc2a-4a04-b250-5cb920921a10
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetFile::CInternetFile
This member function is called when a `CInternetFile` object is created.  
  
## Syntax  
  
```  
  
      CInternetFile(   
   HINTERNET hFile,   
   LPCTSTR pstrFileName,   
   CInternetConnection* pConnection,   
   BOOL bReadMode    
);  
CInternetFile(   
   HINTERNET hFile,   
   HINTERNET hSession,   
   LPCTSTR pstrFileName,   
   LPCTSTR pstrServer,   
   DWORD_PTR dwContext,   
   BOOL bReadMode   
);  
```  
  
#### Parameters  
 `hFile`  
 A handle to an Internet file.  
  
 `pstrFileName`  
 A pointer to a string containing the file name.  
  
 `pConnection`  
 A pointer to a [CInternetConnection](../vs140/CInternetConnection-Class.md) object.  
  
 *bReadMode*  
 Indicates whether the file is read-only.  
  
 `hSession`  
 A handle to an Internet session.  
  
 `pstrServer`  
 A pointer to a string containing the name of the server.  
  
 `dwContext`  
 The context identifier for the `CInternetFile` object. See [WinInet Basics](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Remarks  
 You never create a `CInternetFile` object directly. Instead, create an object of one of its derived classes by calling [CGopherConnection::OpenFile](../vs140/CGopherConnection--OpenFile.md) or [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md). You also can create a `CInternetFile` object by calling [CFtpConnection::OpenFile](../vs140/CFtpConnection--OpenFile.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)   
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [CGopherFile Class](../vs140/CGopherFile-Class.md)