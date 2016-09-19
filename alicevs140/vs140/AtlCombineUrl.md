---
title: "AtlCombineUrl"
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
ms.assetid: c5bb1b78-6eb3-4a27-92ad-0e48d8d5846a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlCombineUrl
Call this function to combine a base URL and a relative URL into a single, canonical URL.  
  
## Syntax  
  
```  
  
      inline BOOL AtlCombineUrl(  
   LPCTSTR szBaseUrl,  
   LPCTSTR szRelativeUrl,  
   LPTSTR szBuffer,  
   DWORD* pdwMaxLength,  
   DWORD dwFlags = 0   
) throw( );  
```  
  
#### Parameters  
 *szBaseUrl*  
 The base URL.  
  
 *szRelativeUrl*  
 The URL relative to the base URL.  
  
 `szBuffer`  
 Caller-allocated buffer to receive the canonicalized URL.  
  
 `pdwMaxLength`  
 Pointer to a variable that contains the length in characters of `szBuffer`. If the function succeeds, the variable receives the number of characters written to the buffer not including the terminating null character. If the function fails, the variable receives the required length in bytes of the buffer including space for the terminating null character.  
  
 `dwFlags`  
 Flags controlling the behavior of this function. See [ATL_URL Flags](../vs140/ATL_URL-Flags.md).  
  
## Return Value  
 Returns **TRUE** on success, **FALSE** on failure.  
  
## Remarks  
 Behaves like the current version of [InternetCombineUrl](http://msdn.microsoft.com/library/windows/desktop/aa384355) but does not require WinInet or Internet Explorer to be installed.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)   
 [InternetCombineUrl](http://msdn.microsoft.com/library/windows/desktop/aa384355)