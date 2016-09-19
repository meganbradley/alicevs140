---
title: "CHttpFile::QueryInfo"
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
ms.assetid: 83946d8e-05a0-49e9-8a1b-5e877ade4c9a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpFile::QueryInfo
Call this member function to return response or request headers from an HTTP request.  
  
## Syntax  
  
```  
  
      BOOL QueryInfo(  
   DWORD dwInfoLevel,  
   LPVOID lpvBuffer,  
   LPDWORD lpdwBufferLength,  
   LPDWORD lpdwIndex = NULL   
) const;  
BOOL QueryInfo(  
   DWORD dwInfoLevel,  
   CString& str,  
   LPDWORD dwIndex = NULL   
) const;  
BOOL QueryInfo(  
   DWORD dwInfoLevel,  
   SYSTEMTIME* pSysTime,  
   LPDWORD dwIndex = NULL   
) const;  
```  
  
#### Parameters  
 `dwInfoLevel`  
 A combination of the attribute to query and the following flags that specify the type of information requested:  
  
-   **HTTP_QUERY_CUSTOM** Finds the header name and returns this value in `lpvBuffer` on output. **HTTP_QUERY_CUSTOM** throws an assertion if the header isn't found.  
  
-   **HTTP_QUERY_FLAG_REQUEST_HEADERS** Typically, the application queries the response headers, but an application can also query request headers by using this flag.  
  
-   **HTTP_QUERY_FLAG_SYSTEMTIME** For those headers whose value is a date/time string, such as "Last-Modified-Time," this flag returns the header value as a standard Win32 [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure that does not require the application to parse the data. If you use this flag, you may want to use the `SYSTEMTIME` override of the function.  
  
-   **HTTP_QUERY_FLAG_NUMBER** For those headers whose value is a number, such as the status code, this flag returns the data as a 32-bit number.  
  
 See the **Remarks** section for a list of the possible values.  
  
 `lpvBuffer`  
 A pointer to the buffer that receives the information.  
  
 `lpdwBufferLength`  
 On entry, this points to a value containing the length of the data buffer, in number of characters or bytes. See the **Remarks** section for more detailed information about this parameter.  
  
 `lpdwIndex`  
 A pointer to a zero-based header index. Can be **NULL**. Use this flag to enumerate multiple headers with the same name. On input, `lpdwIndex` indicates the index of the specified header to return. On output, `lpdwIndex` indicates the index of the next header. If the next index cannot be found, **ERROR_HTTP_HEADER_NOT_FOUND** is returned.  
  
 `str`  
 A reference to the [CString](../vs140/CStringT-Class.md) object receiving the returned information.  
  
 `dwIndex`  
 An index value. See `lpdwIndex`.  
  
 *pSysTime*  
 A pointer to a Win32 [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Remarks  
 Use this member function only after a successful call to [SendRequest](../vs140/CHttpFile--SendRequest.md) or on a `CHttpFile` object successfully created by [OpenURL](../vs140/CInternetSession--OpenURL.md).  
  
 You can retrieve the following types of data from `QueryInfo`:  
  
-   strings (default)  
  
-   `SYSTEMTIME` (for "Data:" "Expires:" etc, headers)  
  
-   `DWORD` (for **STATUS_CODE**, **CONTENT_LENGTH**, etc.)  
  
 When a string is written to the buffer, and the member function succeeds, `lpdwBufferLength` contains the length of the string in characters minus 1 for the terminating **NULL** character.  
  
 The possible `dwInfoLevel` values include:  
  
-   **HTTP_QUERY_MIME_VERSION**  
  
-   **HTTP_QUERY_CONTENT_TYPE**  
  
-   **HTTP_QUERY_CONTENT_TRANSFER_ENCODING**  
  
-   **HTTP_QUERY_CONTENT_ID**  
  
-   **HTTP_QUERY_CONTENT_DESCRIPTION**  
  
-   **HTTP_QUERY_CONTENT_LENGTH**  
  
-   **HTTP_QUERY_ALLOWED_METHODS**  
  
-   **HTTP_QUERY_PUBLIC_METHODS**  
  
-   **HTTP_QUERY_DATE**  
  
-   **HTTP_QUERY_EXPIRES**  
  
-   **HTTP_QUERY_LAST_MODIFIED**  
  
-   **HTTP_QUERY_MESSAGE_ID**  
  
-   **HTTP_QUERY_URI**  
  
-   **HTTP_QUERY_DERIVED_FROM**  
  
-   **HTTP_QUERY_LANGUAGE**  
  
-   **HTTP_QUERY_COST**  
  
-   **HTTP_QUERY_WWW_LINK**  
  
-   **HTTP_QUERY_PRAGMA**  
  
-   **HTTP_QUERY_VERSION**  
  
-   **HTTP_QUERY_STATUS_CODE**  
  
-   **HTTP_QUERY_STATUS_TEXT**  
  
-   **HTTP_QUERY_RAW_HEADERS**  
  
-   **HTTP_QUERY_RAW_HEADERS_CRLF**  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [CHttpConnection::OpenRequest](../vs140/CHttpConnection--OpenRequest.md)   
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [CGopherConnection Class](../vs140/CGopherConnection-Class.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)