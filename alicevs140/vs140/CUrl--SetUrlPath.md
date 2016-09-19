---
title: "CUrl::SetUrlPath"
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
ms.assetid: 069f0f5e-675c-45ea-a121-8c0c3425813f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetUrlPath
Call this method to set the URL path.  
  
## Syntax  
  
```  
  
      inline BOOL SetUrlPath(  
   LPCTSTR lpszPath   
) throw( );  
```  
  
#### Parameters  
 `lpszPath`  
 The URL path.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetUrlPath](../vs140/CUrl--GetUrlPath.md)