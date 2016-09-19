---
title: "CAccessToken::GetProfile"
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
ms.assetid: 0a502ec8-3312-4bf7-bb8a-55a37b8c571f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetProfile
Call this method to get the handle pointing to the user profile associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
HANDLE GetProfile( ) const throw( );  
  
```  
  
## Return Value  
 Returns a handle pointing to the user profile, or NULL if no profile exists.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)