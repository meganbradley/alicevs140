---
title: "CHttpFile::SendRequestEx"
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
ms.assetid: 28e3ab8e-00f5-4ef2-a21e-46890dfd1710
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpFile::SendRequestEx
Call this member function to send a request to an HTTP server.  
  
## Syntax  
  
```  
  
      BOOL SendRequestEx(  
   DWORD dwTotalLen,  
   DWORD dwFlags = HSR_INITIATE,  
   DWORD_PTR dwContext = 1   
);  
BOOL SendRequestEx(  
   LPINTERNET_BUFFERS lpBuffIn,  
   LPINTERNET_BUFFERS lpBuffOut,  
   DWORD dwFlags = HSR_INITIATE,  
   DWORD_PTR dwContext = 1   
);  
```  
  
#### Parameters  
 *dwTotalLen*  
 Number of bytes to be sent in the request.  
  
 `dwFlags`  
 Flags describing the operation. For a list of appropriate flags, see [HttpSendRequestEx](http://msdn.microsoft.com/library/windows/desktop/aa384318) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]*.*  
  
 `dwContext`  
 The context identifier for the `CHttpFile` operation. See Remarks for more information about this parameter.  
  
 `lpBuffIn`  
 Pointer to an initialized [INTERNET_BUFFERS](http://msdn.microsoft.com/library/windows/desktop/aa385132) that describes the input buffer used for the operation.  
  
 *lpBuffOut*  
 Pointer to an initialized **INTERNET_BUFFERS** that describes the output buffer used for the operation.  
  
## Return Value  
 Nonzero if successful. If the call fails, determine the cause of the failure by examining the thrown [CInternetException](../vs140/CInternetException-Class.md) object.  
  
## Remarks  
 This function allows your application to send data using the [Write](../vs140/CInternetFile--Write.md) and [WriteString](../vs140/CInternetFile--WriteString.md) methods of `CInternetFile`. You must know the length of the data to send before calling either override of this function. The first override allows you to specify the length of data you'd like to send. The second override accepts pointers to **INTERNET_BUFFERS** structures, which can be used to describe the buffer in great detail.  
  
 After content is written to the file, call [EndRequest](../vs140/CHttpFile--EndRequest.md) to end the operation.  
  
 The default value for `dwContext` is sent by MFC to the `CHttpFile` object from the [CInternetSession](../vs140/CInternetSession-Class.md) object that created the `CHttpFile` object. When you call [CInternetSession::OpenURL](../vs140/CInternetSession--OpenURL.md) or [CHttpConnection](../vs140/CHttpConnection-Class.md) to construct a `CHttpFile` object, you can override the default to set the context identifier to a value of your choosing. The context identifier is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to provide status on the object with which it is identified. See the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Example  
 This code fragment sends the content of a string to a DLL named MFCISAPI.DLL on the LOCALHOST server. While this example uses only one call to `WriteString`, using multiple calls to send data in blocks is acceptable.  
  
 [!CODE [NVC_MFCWinInet#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWinInet#9)]  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [CHttpFile::SendRequest](../vs140/CHttpFile--SendRequest.md)