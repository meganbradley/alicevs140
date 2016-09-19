---
title: "CFtpConnection::RemoveDirectory"
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
ms.assetid: 89e3924e-19de-44df-b33f-8e275ff41555
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpConnection::RemoveDirectory
Call this member function to remove the specified directory from the connected server.  
  
## Syntax  
  
```  
  
      BOOL RemoveDirectory(  
   LPCTSTR pstrDirName   
);  
```  
  
#### Parameters  
 `pstrDirName`  
 A pointer to a string containing the directory to be removed.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Remarks  
 Use [GetCurrentDirectory](../vs140/CFtpConnection--GetCurrentDirectory.md) to determine the server's current working directory. Do not assume that the remote system has connected you to the root directory.  
  
 The `pstrDirName` parameter can be either a partially or fully qualified filename relative to the current directory. A backslash (\\) or forward slash (/) can be used as the directory separator for either name. `RemoveDirectory` translates the directory name separators to the appropriate characters before they are used.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)