---
title: "CAccessToken::Impersonate"
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
ms.assetid: 3b79d270-4f56-45f0-9949-afe9555bc74e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::Impersonate
Call this method to assign an impersonation `CAccessToken` to a thread.  
  
## Syntax  
  
```  
  
      bool Impersonate(  
   HANDLE hThread = NULL  
) const throw(...);  
```  
  
#### Parameters  
 `hThread`  
 Handle to the thread to assign the impersonation token to. This handle must have been opened with TOKEN_IMPERSONATE access rights. If `hThread` is NULL, the method causes the thread to stop using an impersonation token.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 In debug builds, an assertion error will occur if `CAccessToken` does not have a valid pointer to a token.  
  
 The [CAutoRevertImpersonation class](../vs140/CAutoRevertImpersonation-Class.md) can be used to automatically revert impersonated access tokens.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)