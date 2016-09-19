---
title: "CUrl::CrackUrl"
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
ms.assetid: b79997e9-22af-4571-86d5-f0c71f3bca2c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::CrackUrl
Call this method to decode and parse the URL.  
  
## Syntax  
  
```  
  
      BOOL CrackUrl(  
   LPCTSTR lpszUrl,  
   DWORD dwFlags = 0   
) throw( );  
```  
  
#### Parameters  
 `lpszUrl`  
 The URL.  
  
 `dwFlags`  
 Specify ATL_URL_DECODE or ATL_URL_ESCAPE to convert all escape characters in `lpszUrl` to their real values after parsing. (Before Visual C++ 2005, ATL_URL_DECODE converted all escape characters before parsing.)  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)