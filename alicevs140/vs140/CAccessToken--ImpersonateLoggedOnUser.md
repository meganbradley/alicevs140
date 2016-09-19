---
title: "CAccessToken::ImpersonateLoggedOnUser"
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
ms.assetid: 6517b837-1b1b-42d8-bcb2-d06899efedcd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::ImpersonateLoggedOnUser
Call this method to allow the calling thread to impersonate the security context of a logged-on user.  
  
## Syntax  
  
```  
  
bool ImpersonateLoggedOnUser( ) const throw(...);  
  
```  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
  
> [!IMPORTANT]
>  If a call to an impersonation function fails for any reason, the client is not impersonated and the client request is made in the security context of the process from which the call was made. If the process is running as a highly privileged account, or as a member of an administrative group, the user might be able to perform actions he or she would otherwise be disallowed. Therefore, the return value for this function should always be confirmed.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::LoadUserProfile](../vs140/CAccessToken--LoadUserProfile.md)   
 [CAccessToken::LogonUser](../vs140/CAccessToken--LogonUser.md)