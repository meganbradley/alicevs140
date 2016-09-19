---
title: "CInternetSession::SetOption"
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
ms.assetid: 4c30d846-9c8a-4e7c-a0f3-11fb7b1ef040
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetSession::SetOption
Call this member function to set options for the Internet session.  
  
## Syntax  
  
```  
  
      BOOL SetOption(  
   DWORD dwOption,  
   LPVOID lpBuffer,  
   DWORD dwBufferLength,  
   DWORD dwFlags = 0   
);  
BOOL SetOption(  
   DWORD dwOption,  
   DWORD dwValue,  
   DWORD dwFlags = 0   
);  
```  
  
#### Parameters  
 `dwOption`  
 The Internet option to set. See [Option Flags](http://msdn.microsoft.com/library/windows/desktop/aa385328) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]for a list of the possible options.  
  
 `lpBuffer`  
 A buffer that contains the option setting.  
  
 *dwBufferLength*  
 The length of `lpBuffer` or the size of `dwValue`.  
  
 `dwValue`  
 A `DWORD` that contains the option setting.  
  
 `dwFlags`  
 Indicates various caching options. The default is set to 0. The possible values include:  
  
-   `INTERNET_FLAG_DONT_CACHE` Do not cache the data, either locally or in any gateway servers.  
  
-   `INTERNET_FLAG_OFFLINE` Download operations are satisfied through the persistent cache only. If the item does not exist in the cache, an appropriate error code is returned. This flag may be combined with the bitwise `OR` (**&#124;**) operator.  
  
## Return Value  
 If the operation was successful, a value of **TRUE** is returned. If an error occurred, a value of **FALSE** is returned. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetSession Class](../vs140/CInternetSession-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetSession::ServiceTypeFromHandle](assetId:///00458651-5aea-4788-bc37-9fc45f731a80)