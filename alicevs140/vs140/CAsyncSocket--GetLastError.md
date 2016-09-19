---
title: "CAsyncSocket::GetLastError"
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
ms.assetid: ff1a1772-5abb-426b-afc6-6cdef8442c70
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAsyncSocket::GetLastError
Call this member function to get the error status for the last operation that failed.  
  
## Syntax  
  
```  
  
static int PASCAL GetLastError( );  
```  
  
## Return Value  
 The return value indicates the error code for the last Windows Sockets API routine performed by this thread.  
  
## Remarks  
 When a particular member function indicates that an error has occurred, `GetLastError` should be called to retrieve the appropriate error code. See the individual member function descriptions for a list of applicable error codes.  
  
 For more information about the error codes, see [Windows Sockets 2 API](http://msdn.microsoft.com/library/windows/desktop/ms740673).  
  
## Requirements  
 **Header:** afxsock.h  
  
## See Also  
 [CAsyncSocket Class](../vs140/CAsyncSocket-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WSASetLastError](http://msdn.microsoft.com/library/windows/desktop/ms742209)