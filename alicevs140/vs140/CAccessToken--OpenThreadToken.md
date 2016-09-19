---
title: "CAccessToken::OpenThreadToken"
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
ms.assetid: 4dfbf21e-82cf-4aae-be47-570f8453e620
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::OpenThreadToken
Call this method to set the impersonation level and then initialize the `CAccessToken` with the token from the given thread.  
  
## Syntax  
  
```  
  
      bool OpenThreadToken(  
   DWORD dwDesiredAccess,  
   bool bImpersonate = false,  
   bool bOpenAsSelf = true,  
   SECURITY_IMPERSONATION_LEVEL sil = SecurityImpersonation  
) throw(...);  
```  
  
#### Parameters  
 `dwDesiredAccess`  
 Specifies an access mask that specifies the requested types of access to the access token. These requested access types are compared with the token's DACL to determine which accesses are granted or denied.  
  
 `bImpersonate`  
 If true, the thread will be left at the requested impersonation level after this method completes. If false, the thread will revert to its original impersonation level.  
  
 `bOpenAsSelf`  
 Indicates whether the access check is to be made against the security context of the thread calling the [GetThreadToken](http://msdn.microsoft.com/library/windows/desktop/ms683182) method or against the security context of the process for the calling thread.  
  
 If this parameter is false, the access check is performed using the security context for the calling thread. If the thread is impersonating a client, this security context can be that of a client process. If this parameter is true, the access check is made using the security context of the process for the calling thread.  
  
 `sil`  
 Specifies a [SECURITY_IMPERSONATION_LEVEL](http://msdn.microsoft.com/library/windows/desktop/aa379572) enumerated type that supplies the impersonation level of the token.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 `OpenThreadToken` is similar to [CAccessToken::GetThreadToken](../vs140/CAccessToken--GetThreadToken.md), but sets the impersonation level before initializing the `CAccessToken` from the thread's access token.  
  
 The [CAutoRevertImpersonation Class](../vs140/CAutoRevertImpersonation-Class.md) can be used to automatically revert impersonated access tokens created by setting the `bImpersonate` flag to *true*.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::GetThreadToken](../vs140/CAccessToken--GetThreadToken.md)