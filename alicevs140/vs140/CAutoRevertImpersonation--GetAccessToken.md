---
title: "CAutoRevertImpersonation::GetAccessToken"
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
ms.assetid: 55160184-6639-442c-ae18-cb4a5ebca2c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoRevertImpersonation::GetAccessToken
Retrieves the access token current associated with this object.  
  
## Syntax  
  
```  
  
const CAccessToken* GetAccessToken() throw( );  
  
```  
  
## Return Value  
 The address of the previously associated [CAccessToken](../vs140/CAccessToken-Class.md), or NULL if no association existed.  
  
## Remarks  
 If this method is called for the purposes that include the reversion of an impersonation of the `CAccessToken` object, the [Detach](../vs140/CAutoRevertImpersonation--Detach.md) method should be used instead.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAutoRevertImpersonation Class](../vs140/CAutoRevertImpersonation-Class.md)   
 [CAccessToken Class](../vs140/CAccessToken-Class.md)