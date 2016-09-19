---
title: "CInternetSession::GetCookieLength"
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
ms.assetid: 2f24ebcc-e85a-44fe-b303-8ea21990cbc2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::GetCookieLength
Call this member function to get the length of the cookie stored in the buffer.  
  
## Syntax  
  
```  
  
      static DWORD GetCookieLength(  
   LPCTSTR pstrUrl,  
   LPCTSTR pstrCookieName   
);  
```  
  
#### Parameters  
 `pstrUrl`  
 A pointer to a string containing the URL  
  
 `pstrCookieName`  
 A pointer to a string containing the name of the cookie.  
  
## Return Value  
 A `DWORD` value indicating the length of the cookie, stored in the buffer. Zero if no cookie with the name indicated by `pstrCookieName` exists.  
  
## Remarks  
 This value is used by [GetCookie](../vs140/CInternetSession--GetCookie.md).  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetSession::SetCookie](../vs140/CInternetSession--SetCookie.md)