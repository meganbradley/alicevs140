---
title: "AfxGetInternetHandleType"
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
ms.assetid: 754d6b3c-4eee-4190-8688-e4fb0381e92f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxGetInternetHandleType
Use this global function to determine the type of an Internet handle.  
  
## Syntax  
  
```  
  
      DWORD AFXAPI AfxGetInternetHandleType(  
 HINTERNET hQuery   
);  
```  
  
#### Parameters  
 `hQuery`  
 A handle to an Internet query.  
  
## Return Value  
 Any of the Internet service types defined by WININET.H. See the Remarks section for a list of these Internet services. If the handle is NULL or not recognized, the function returns AFX_INET_SERVICE_UNK.  
  
## Remarks  
 The following list includes possible Internet types returned by `AfxGetInternetHandleType`.  
  
-   INTERNET_HANDLE_TYPE_INTERNET  
  
-   INTERNET_HANDLE_TYPE_CONNECT_FTP  
  
-   INTERNET_HANDLE_TYPE_CONNECT_GOPHER  
  
-   INTERNET_HANDLE_TYPE_CONNECT_HTTP  
  
-   INTERNET_HANDLE_TYPE_FTP_FIND  
  
-   INTERNET_HANDLE_TYPE_FTP_FIND_HTML  
  
-   INTERNET_HANDLE_TYPE_FTP_FILE  
  
-   INTERNET_HANDLE_TYPE_FTP_FILE_HTML  
  
-   INTERNET_HANDLE_TYPE_GOPHER_FIND  
  
-   INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML  
  
-   INTERNET_HANDLE_TYPE_GOPHER_FILE  
  
-   INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML  
  
-   INTERNET_HANDLE_TYPE_HTTP_REQUEST  
  
> [!NOTE]
>  In order to call this function, your project must include AFXINET.H.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxParseURL](../vs140/AfxParseURL.md)