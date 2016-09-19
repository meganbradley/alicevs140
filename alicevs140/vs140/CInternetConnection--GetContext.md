---
title: "CInternetConnection::GetContext"
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
ms.assetid: e6384594-622d-4e36-9672-7503b40c2a08
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetConnection::GetContext
Call this member function to get the context ID for this session.  
  
## Syntax  
  
```  
  
DWORD_PTR GetContext( ) const;  
  
```  
  
## Return Value  
 The application-assigned context ID.  
  
## Remarks  
 The context ID is originally specified in [CInternetSession](../vs140/CInternetSession-Class.md) and propagates to `CInternetConnection`- and [CInternetFile](../vs140/CInternetFile-Class.md)-derived classes, unless specified differently in the call to a function that opens the connection. The context ID is associated with any operation of the given object and identifies the operation's status information returned by [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md).  
  
 For more information about how **GetContext** works with other WinInet classes to give the user status information, see the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md) for more information about the context identifier.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetSession::EnableStatusCallback](../vs140/CInternetSession--EnableStatusCallback.md)