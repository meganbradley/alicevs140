---
title: "CHttpFile::QueryInfoStatusCode"
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
ms.assetid: 49b3487d-8ecf-4571-ac5f-2ad29286d863
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpFile::QueryInfoStatusCode
Call this member function to get the status code associated with an HTTP request and place it in the supplied `dwStatusCode` parameter.  
  
## Syntax  
  
```  
  
      BOOL QueryInfoStatusCode(  
   DWORD& dwStatusCode   
) const;  
```  
  
#### Parameters  
 `dwStatusCode`  
 A reference to a status code. Status codes indicate the success or failure of the requested event. See **Remarks** for a selection of status code descriptions.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Remarks  
 Use this member function only after a successful call to [SendRequest](../vs140/CHttpFile--SendRequest.md) or on a `CHttpFile` object successfully created by [OpenURL](../vs140/CInternetSession--OpenURL.md).  
  
 HTTP status codes fall into groups indicating the success or failure of the request. The following tables outline the status code groups and the most common HTTP status codes.  
  
|Group|Meaning|  
|-----------|-------------|  
|200-299|Success|  
|300-399|Information|  
|400-499|Request error|  
|500-599|Server error|  
  
 Common HTTP Status Codes:  
  
|Status code|Meaning|  
|-----------------|-------------|  
|200|URL located, transmission follows|  
|400|Unintelligible request|  
|404|Requested URL not found|  
|405|Server does not support requested method|  
|500|Unknown server error|  
|503|Server capacity reached|  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)