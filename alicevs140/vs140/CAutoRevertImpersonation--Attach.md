---
title: "CAutoRevertImpersonation::Attach"
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
ms.assetid: 57944c5b-5394-43ee-83cb-8743e9b01141
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoRevertImpersonation::Attach
Automates the impersonation reversion of an access token.  
  
## Syntax  
  
```  
  
      void Attach(   
   const CAccessToken* pAT   
) throw( );  
```  
  
#### Parameters  
 `pAT`  
 The address of the [CAccessToken](../vs140/CAccessToken-Class.md) object to be reverted automatically  
  
## Remarks  
 This method should only be used if the [CAutoRevertImpersonation](../vs140/CAutoRevertImpersonation-Class.md) object was created with a NULL `CAccessToken` pointer, or if [Detach](../vs140/CAutoRevertImpersonation--Detach.md) was called previously. For simple cases, it is not necessary to use this method.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAutoRevertImpersonation Class](../vs140/CAutoRevertImpersonation-Class.md)   
 [CAccessToken Class](../vs140/CAccessToken-Class.md)