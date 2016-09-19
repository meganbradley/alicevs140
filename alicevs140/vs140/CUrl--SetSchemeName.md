---
title: "CUrl::SetSchemeName"
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
ms.assetid: 0ff0ca79-11a4-45ee-8680-8d2c10511f73
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CUrl::SetSchemeName
Call this method to set the URL scheme name.  
  
## Syntax  
  
```  
  
      inline BOOL SetSchemeName(  
   LPCTSTR lpszSchm   
) throw( );  
```  
  
#### Parameters  
 *lpszSchm*  
 The URL scheme name.  
  
## Return Value  
 Returns TRUE on success, FALSE on failure.  
  
## Remarks  
 You can also set the scheme by using an [ATL_URL_SCHEME](../vs140/ATL_URL_SCHEME.md) constant (see [CUrl::SetScheme](../vs140/CUrl--SetScheme.md)).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CUrl Class](../vs140/CUrl-Class.md)   
 [CUrl::GetSchemeName](../vs140/CUrl--GetSchemeName.md)