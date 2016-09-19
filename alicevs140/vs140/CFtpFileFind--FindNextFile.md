---
title: "CFtpFileFind::FindNextFile"
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
ms.assetid: 38e09283-f4b7-4434-a7f2-da92363254d0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpFileFind::FindNextFile
Call this member function to continue a file search begun with a call to the [FindFile](../vs140/CFtpFileFind--FindFile.md) member function.  
  
## Syntax  
  
```  
  
virtual BOOL FindNextFile( );  
  
```  
  
## Return Value  
 Nonzero if there are more files; zero if the file found is the last one in the directory or if an error occurred. To get extended error information, call the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360). If the file found is the last file in the directory, or if no matching files can be found, the `GetLastError` function returns ERROR_NO_MORE_FILES.  
  
## Remarks  
 You must call this function at least once before calling any attribute function (see [CFileFind::FindNextFile](../vs140/CFileFind--FindNextFile.md)).  
  
 `FindNextFile` wraps the Win32 function [FindNextFile](http://msdn.microsoft.com/library/windows/desktop/aa364428).  
  
## Example  
 See the example in the [CFtpFileFind](../vs140/CFtpFileFind-Class.md) class overview.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpFileFind Class](../vs140/CFtpFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind Class](../vs140/CFileFind-Class.md)