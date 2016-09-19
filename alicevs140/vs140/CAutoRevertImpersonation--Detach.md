---
title: "CAutoRevertImpersonation::Detach"
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
ms.assetid: 9309fae5-577d-4018-830e-e763a4df37f7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoRevertImpersonation::Detach
Cancels the automatic impersonation reversion.  
  
## Syntax  
  
```  
  
const CAccessToken* Detach() throw( );  
  
```  
  
## Return Value  
 The address of the previously associated [CAccessToken](../vs140/CAccessToken-Class.md), or NULL if no association existed.  
  
## Remarks  
 Calling **Detach** prevents the `CAutoRevertImpersonation` object from reverting any impersonation currently in effect for the [CAccessToken](../vs140/CAccessToken-Class.md) object associated with this object. `CAutoRevertImpersonation` can then be destroyed with no effect or reassociated to the same or another `CAccessToken` object using [Attach](../vs140/CAutoRevertImpersonation--Attach.md).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAutoRevertImpersonation Class](../vs140/CAutoRevertImpersonation-Class.md)   
 [CAccessToken Class](../vs140/CAccessToken-Class.md)