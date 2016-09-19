---
title: "CFtpConnection::GetCurrentDirectory"
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
ms.assetid: 2e898544-72ca-469e-b083-eb6288dfe0f0
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpConnection::GetCurrentDirectory
Call this member function to get the name of the current directory.  
  
## Syntax  
  
```  
  
      BOOL GetCurrentDirectory(  
   CString& strDirName   
) const;  
BOOL GetCurrentDirectory(  
   LPTSTR pstrDirName,  
   LPDWORD lpdwLen   
) const;  
```  
  
#### Parameters  
 `strDirName`  
 A reference to a string that will receive the name of the directory.  
  
 `pstrDirName`  
 A pointer to a string that will receive the name of the directory.  
  
 `lpdwLen`  
 A pointer to a DWORD that contains the following information:  
  
|||  
|-|-|  
|On entry|The size of the buffer referenced by `pstrDirName`.|  
|On return|The number of characters stored to `pstrDirName`. If the member function fails and ERROR_INSUFFICIENT_BUFFER is returned, then `lpdwLen` contains the number of bytes that the application must allocate in order to receive the string.|  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Remarks  
 To get the directory name as a URL instead, call [GetCurrentDirectoryAsURL](../vs140/CFtpConnection--GetCurrentDirectoryAsURL.md).  
  
 The parameters `pstrDirName` or `strDirName` can be either partially qualified filenames relative to the current directory or fully qualified. A backslash (\\) or forward slash (/) can be used as the directory separator for either name. `GetCurrentDirectory` translates the directory name separators to the appropriate characters before they are used.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFtpConnection::GetCurrentDirectoryAsURL](../vs140/CFtpConnection--GetCurrentDirectoryAsURL.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)