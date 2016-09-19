---
title: "CHttpFile::EndRequest"
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
ms.assetid: e58e4478-8416-4985-9a07-c5152ea719a8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHttpFile::EndRequest
Call this member function to end a request sent to an HTTP server with the [SendRequestEx](../vs140/CHttpFile--SendRequestEx.md) member function.  
  
## Syntax  
  
```  
  
      BOOL EndRequest(  
   DWORD dwFlags = 0,  
   LPINTERNET_BUFFERS lpBuffIn = NULL,  
   DWORD_PTR dwContext = 1   
);  
```  
  
#### Parameters  
 `dwFlags`  
 Flags describing the operation. For a list of the appropriate flags, see [HttpEndRequest](http://msdn.microsoft.com/library/windows/desktop/aa384230) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `lpBuffIn`  
 Pointer to an initialized [INTERNET_BUFFERS](http://msdn.microsoft.com/library/windows/desktop/aa385132) that describes the input buffer used for the operation.  
  
 `dwContext`  
 The context identifier for the `CHttpFile` operation. See Remarks for more information about this parameter.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, determine the cause of the failure by examining the thrown [CInternetException](../vs140/CInternetException-Class.md) object.  
  
## Remarks  
 The default value for `dwContext` is sent by MFC to the `CHttpFile` object from the [CInternetSession](../vs140/CInternetSession-Class.md) object that created the `CHttpFile` object. When you call [CInternetSession::OpenURL](../vs140/CInternetSession--OpenURL.md) or [CHttpConnection](../vs140/CHttpConnection-Class.md) to construct a `CHttpFile` object, you can override the default to set the context identifier to a value of your choosing. The context identifier is returned to [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) to provide status on the object with which it is identified. See article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CHttpFile Class](../vs140/CHttpFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetFile Class](../vs140/CInternetFile-Class.md)