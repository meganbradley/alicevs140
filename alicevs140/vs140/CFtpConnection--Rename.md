---
title: "CFtpConnection::Rename"
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
ms.assetid: a093d9d8-7287-42fe-b710-d4476ade9eda
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFtpConnection::Rename
Call this member function to rename the specified file on the connected server.  
  
## Syntax  
  
```  
  
      BOOL Rename(  
   LPCTSTR pstrExisting,  
   LPCTSTR pstrNew   
);  
```  
  
#### Parameters  
 `pstrExisting`  
 A pointer to a string containing the current name of the file to be renamed.  
  
 `pstrNew`  
 A pointer to a string containing the file's new name.  
  
## Return Value  
 Nonzero if successful; otherwise 0. If the call fails, the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360) may be called to determine the cause of the error.  
  
## Remarks  
 The `pstrExisting` and `pstrNew` parameters can be either a partially qualified filename relative to the current directory or fully qualified. A backslash (\\) or forward slash (/) can be used as the directory separator for either name. **Rename** translates the directory name separators to the appropriate characters before they are used.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CFtpConnection Class](../vs140/CFtpConnection-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CInternetConnection Class](../vs140/CInternetConnection-Class.md)