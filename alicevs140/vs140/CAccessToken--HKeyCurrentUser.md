---
title: "CAccessToken::HKeyCurrentUser"
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
ms.assetid: 393cd679-aa77-4f71-8dec-67bb9beb6652
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::HKeyCurrentUser
Call this method to get the handle pointing to the user profile associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
HKEY HKeyCurrentUser( ) const throw( );  
  
```  
  
## Return Value  
 Returns a handle pointing to the user profile, or NULL if no profile exists.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::LoadUserProfile](../vs140/CAccessToken--LoadUserProfile.md)