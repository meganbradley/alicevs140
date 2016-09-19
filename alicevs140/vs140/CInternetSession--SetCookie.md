---
title: "CInternetSession::SetCookie"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 3d646dc2-cea7-4d29-bd6f-982283da207c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::SetCookie
Sets a cookie for the specified URL.  
  
## Syntax  
  
```  
  
      static BOOL SetCookie(  
   LPCTSTR pstrUrl,  
   LPCTSTR pstrCookieName,  
   LPCTSTR pstrCookieData   
);  
```  
  
#### Parameters  
 `pstrUrl`  
 A pointer to a null-terminated string that specifies the URL for which the cookie should be set.  
  
 `pstrCookieName`  
 A pointer to a string containing the name of the cookie.  
  
 `pstrCookieData`  
 A pointer to a string containing the actual string data to associate with the URL.  
  
## Return Value  
 Returns **TRUE** if successful, or **FALSE** otherwise. To get the specific error code, call **GetLastError.**  
  
## Remarks  
 This member function implements the behavior of the Win32 message [InternetSetCookie](http://msdn.microsoft.com/library/windows/desktop/aa385107), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession::GetCookieLength](../vs140/CInternetSession--GetCookieLength.md)   
 [CInternetSession::GetCookie](../vs140/CInternetSession--GetCookie.md)