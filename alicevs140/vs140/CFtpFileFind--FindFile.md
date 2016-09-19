---
title: "CFtpFileFind::FindFile"
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
ms.assetid: 6024590c-465a-4880-bb93-094acaf53375
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpFileFind::FindFile
Call this member function to find an FTP file.  
  
## Syntax  
  
```  
  
      virtual BOOL FindFile(  
   LPCTSTR pstrName = NULL,  
   DWORD dwFlags = INTERNET_FLAG_RELOAD   
);  
```  
  
#### Parameters  
 `pstrName`  
 A pointer to a string containing the name of the file to find. If **NULL**, the call will perform a wildcard search (*).  
  
 `dwFlags`  
 The flags describing how to handle this session. These flags can be combined with the bitwise OR operator (&#124;) and are as follows:  
  
-   INTERNET_FLAG_RELOAD   Get the data from the wire even if it is locally cached. This is the default flag.  
  
-   INTERNET_FLAG_DONT_CACHE   Do not cache the data, either locally or in any gateways.  
  
-   INTERNET_FLAG_RAW_DATA   Override the default to return the raw data ([WIN32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structures for FTP).  
  
-   INTERNET_FLAG_SECURE   Secures transactions on the wire with Secure Sockets Layer or PCT. This flag is applicable to HTTP requests only.  
  
-   INTERNET_FLAG_EXISTING_CONNECT   If possible, reuse the existing connections to the server for new **FindFile** requests instead of creating a new session for each request.  
  
## Return Value  
 Nonzero if successful; otherwise 0. To get extended error information, call the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360).  
  
## Remarks  
 After calling **FindFile** to retrieve the first FTP file, you can call [FindNextFile](../vs140/CFtpFileFind--FindNextFile.md) to retrieve subsequent FTP files.  
  
## Example  
 See the example in the [CFtpFileFind](../vs140/CFtpFileFind-Class.md) class overview.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpFileFind Class](../vs140/CFtpFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFtpFileFind::FindNextFile](../vs140/CFtpFileFind--FindNextFile.md)   
 [CFileFind Class](../vs140/CFileFind-Class.md)