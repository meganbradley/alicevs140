---
title: "CInternetSession::GetContext"
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
ms.assetid: 923e626c-0332-436c-a830-83888f50ae2e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::GetContext
Call this member function to get the context value for a particular application session.  
  
## Syntax  
  
```  
  
DWORD_PTR GetContext( ) const;  
  
```  
  
## Return Value  
 The application-defined context Identifier.  
  
## Remarks  
 [OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md) uses the context ID returned by **GetContext** to report the status of a particular application. For example, when a user activates an Internet request that involves returning status information, the status callback uses the context ID to report status on that particular request. If the user activates two separate Internet requests that both involve returning status information, `OnStatusCallback` uses the context identifiers to return status about their corresponding requests. Consequently, the context identifier is used for all status callback operations, and it is associated with the session until the session is ended.  
  
 For more information about asynchronous operations, see the article [Internet First Steps: WinInet](../vs140/WinInet-Basics.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)   
 [CInternetSession::EnableStatusCallback](../vs140/CInternetSession--EnableStatusCallback.md)   
 [CInternetSession::OnStatusCallback](../vs140/CInternetSession--OnStatusCallback.md)