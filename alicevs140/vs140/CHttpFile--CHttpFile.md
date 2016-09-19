---
title: "CHttpFile::CHttpFile"
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
ms.assetid: 93bc7702-bda1-434b-8d4d-59d67a220454
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpFile::CHttpFile
This member function is called to construct a `CHttpFile` object.  
  
## Syntax  
  
```  
  
      CHttpFile(  
   HINTERNET hFile,  
   HINTERNET hSession,  
   LPCTSTR pstrObject,  
   LPCTSTR pstrServer,  
   LPCTSTR pstrVerb,  
   DWORD_PTR dwContext   
);  
CHttpFile(  
   HINTERNET hFile,  
   LPCTSTR pstrVerb,  
   LPCTSTR pstrObject,  
   CHttpConnection* pConnection   
);  
```  
  
#### Parameters  
 `hFile`  
 A handle to an Internet file.  
  
 `hSession`  
 A handle to an Internet session.  
  
 *pstrObject*  
 A pointer to a string containing the `CHttpFile` object.  
  
 `pstrServer`  
 A pointer to a string containing the name of the server.  
  
 `pstrVerb`  
 A pointer to a string containing the method to be used when sending the request. Can be **POST**, **HEAD**, or `GET`.  
  
 dwContext  
 The context identifier for the `CHttpFile` object. See **Remarks** for more information about this parameter.  
  
 `pConnection`  
 A pointer to a [CHttpConnection](../vs140/CHttpConnection-Class.md) object.  
  
## Remarks  
 You never construct a `CHttpFile` object directly; rather call [CInternetSession::OpenURL](../vs140/CInternetSession--OpenURL.md) or [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md) instead.  
  
 The default value for `dwContext` is sent by MFC to the `CHttpFile` object from the [CInternetSession](../vs140/CInternetSession-Class.md) object that created the `CHttpFile` object. When you call `CInternetSession::OpenURL` or `CHttpConnection` to construct a `CHttpFile` object, you can override the default to set the context identifier to a value of your choosing. The context identifier is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to provide status on the object with which it is identified. See the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)