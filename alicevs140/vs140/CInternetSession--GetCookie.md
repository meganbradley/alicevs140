---
title: "CInternetSession::GetCookie"
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
ms.assetid: 62899a69-0ed8-4340-bd93-88a20d55bb12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::GetCookie
This member function implements the behavior of the Win32 function [InternetGetCookie](http://msdn.microsoft.com/library/windows/desktop/aa384710), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      static BOOL GetCookie(  
   LPCTSTR pstrUrl,  
   LPCTSTR pstrCookieName,  
   LPTSTR pstrCookieData,  
   DWORD dwBufLen   
);  
static BOOL GetCookie(  
   LPCTSTR pstrUrl,  
   LPCTSTR pstrCookieName,  
   CString& strCookieData   
);  
```  
  
#### Parameters  
 `pstrUrl`  
 A pointer to a string containing the URL.  
  
 `pstrCookieName`  
 A pointer to a string containing the name of the cookie to get for the specified URL.  
  
 `pstrCookieData`  
 In the first overload, a pointer to a string containing the address of the buffer that receives the cookie data. This value can be **NULL**. In the second overload, a reference to a [CString](../vs140/CStringT-Class.md) object to receive the cookie data.  
  
 `dwBufLen`  
 The variable specifying the size of the `pstrCookieData` buffer. If the function succeeds, the buffer receives the amount of data copied to the `pstrCookieData` buffer. If `pstrCookieData` is **NULL**, this parameter receives a value that specifies the size of the buffer necessary to copy all the cookie data.  
  
## Return Value  
 Returns **TRUE** if successful, or **FALSE** otherwise. If the call fails, call the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) to determine the cause of the error. The following error values apply:  
  
-   **ERROR_NO_MORE_ITEMS** There is no cookie for the specified URL and all its parents.  
  
-   **ERROR_INSUFFICIENT_BUFFER** The value passed in `dwBufLen` is insufficient to copy all the cookie data. The value returned in `dwBufLen` is the size of the buffer necessary to get all the data.  
  
## Remarks  
 In the second overload, MFC retrieves the cookie data into the supplied `CString` object.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession::GetCookieLength](../vs140/CInternetSession--GetCookieLength.md)   
 [CInternetSession::SetCookie](../vs140/CInternetSession--SetCookie.md)