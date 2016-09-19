---
title: "CAccessToken::LoadUserProfile"
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
ms.assetid: e3182aaf-987a-407d-9dd8-6f40a723bf80
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::LoadUserProfile
Call this method to load the user profile associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
bool LoadUserProfile( ) throw(...);  
  
```  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 In debug builds, an assertion error will occur if the `CAccessToken` does not contain a valid token, or if a user profile already exists.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::ImpersonateLoggedOnUser](../vs140/CAccessToken--ImpersonateLoggedOnUser.md)   
 [CAccessToken::HKeyCurrentUser](../vs140/CAccessToken--HKeyCurrentUser.md)