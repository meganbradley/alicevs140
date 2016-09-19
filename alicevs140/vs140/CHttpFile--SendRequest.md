---
title: "CHttpFile::SendRequest"
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
ms.assetid: e88873d0-2734-491a-bf07-0fe5e5f2c5a3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpFile::SendRequest
Call this member function to send a request to an HTTP server.  
  
## Syntax  
  
```  
  
      BOOL SendRequest(  
   LPCTSTR pstrHeaders = NULL,  
   DWORD dwHeadersLen = 0,  
   LPVOID lpOptional = NULL,  
   DWORD dwOptionalLen = 0   
);  
BOOL SendRequest(  
   CString& strHeaders,  
   LPVOID lpOptional = NULL,  
   DWORD dwOptionalLen = 0   
);  
```  
  
#### Parameters  
 `pstrHeaders`  
 A pointer to a string containing the name of the headers to send.  
  
 `dwHeadersLen`  
 The length of the headers identified by `pstrHeaders`.  
  
 `lpOptional`  
 Any optional data to send immediately after the request headers. This is generally used for **POST** and **PUT** operations. This can be **NULL** if there is no optional data to send.  
  
 *dwOptionalLen*  
 The length of `lpOptional`.  
  
 `strHeaders`  
 A string containing the name of the headers for the request being sent.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, determine the cause of the failure by examining the thrown [CInternetException](../vs140/CInternetException-Class.md) object.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [CHttpFile::SendRequestEx](../vs140/CHttpFile--SendRequestEx.md)