---
title: "CAccessToken::CreateImpersonationToken"
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
ms.assetid: 235f1c1c-50c1-49ba-8b0b-c5b46f5de27b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::CreateImpersonationToken
Call this method to create an impersonation access token.  
  
## Syntax  
  
```  
  
      bool CreateImpersonationToken(  
   CAccessToken* pImp,  
   SECURITY_IMPERSONATION_LEVEL sil = SecurityImpersonation  
) const throw(...);  
```  
  
#### Parameters  
 `pImp`  
 Pointer to the new `CAccessToken` object.  
  
 `sil`  
 Specifies a [SECURITY_IMPERSONATION_LEVEL](http://msdn.microsoft.com/library/windows/desktop/aa379572) enumerated type that supplies the impersonation level of the new token.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 `CreateImpersonationToken` calls [DuplicateToken](http://msdn.microsoft.com/library/windows/desktop/aa446616) to create a new impersonation token.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::CreatePrimaryToken](../vs140/CAccessToken--CreatePrimaryToken.md)   
 [CAccessToken::CreateRestrictedToken](../vs140/CAccessToken--CreateRestrictedToken.md)   
 [CAccessToken::Revert](../vs140/CAccessToken--Revert.md)