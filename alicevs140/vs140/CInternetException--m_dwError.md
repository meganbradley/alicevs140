---
title: "CInternetException::m_dwError"
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
ms.assetid: 175c5e1c-5657-4d07-a206-7d883837481c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetException::m_dwError
The error that caused the exception.  
  
## Syntax  
  
```  
  
DWORD m_dwError;  
  
```  
  
## Remarks  
 This error value may be a system error code, found in WINERROR.H, or an error value from WININET.H.  
  
 For a list of Win32 error codes, see [Error Codes](http://msdn.microsoft.com/library/windows/desktop/ms681381). For a list of Internet-specific error messages, see [Error Messages and Error Pages](_idxs_Error_Messages_and_Error_Pages). Both topics are in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetException Class](../vs140/CInternetException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CException Class](../vs140/CException-Class.md)