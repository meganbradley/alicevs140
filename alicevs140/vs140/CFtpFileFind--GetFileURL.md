---
title: "CFtpFileFind::GetFileURL"
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
ms.assetid: d4089828-1c4b-49f6-8326-ba0000fcffcc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpFileFind::GetFileURL
Call this member function to get the URL of the specified file.  
  
## Syntax  
  
```  
  
CString GetFileURL( ) const;  
  
```  
  
## Return Value  
 The file and path of the Universal Resource Locator (URL).  
  
## Remarks  
 `GetFileURL` is similar to the member function [CFileFind::GetFilePath](../vs140/CFileFind--GetFilePath.md), except that it returns the URL in the form `ftp://moose/dir/file.txt`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpFileFind Class](../vs140/CFtpFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFtpFileFind::FindFile](../vs140/CFtpFileFind--FindFile.md)   
 [CFileFind Class](../vs140/CFileFind-Class.md)