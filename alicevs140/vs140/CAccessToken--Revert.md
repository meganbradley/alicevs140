---
title: "CAccessToken::Revert"
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
ms.assetid: 8d5b191a-9513-4faf-a7da-7b24eb4b509f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::Revert
Call this method to stop a thread from using an impersonation token.  
  
## Syntax  
  
```  
  
      bool Revert(  
   HANDLE hThread = NULL   
) const throw( );  
```  
  
#### Parameters  
 `hThread`  
 Handle to the thread to revert from impersonation. If *hThread* is NULL, the current thread is assumed.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 The reversion of impersonation tokens can be performed automatically with the [CAutoRevertImpersonation Class](../vs140/CAutoRevertImpersonation-Class.md).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::CreateImpersonationToken](../vs140/CAccessToken--CreateImpersonationToken.md)