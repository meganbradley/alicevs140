---
title: "CAccessToken::SetPrimaryGroup"
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
ms.assetid: 379574ab-7f45-46cf-b290-7a67b51ff217
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::SetPrimaryGroup
Call this method to set the primary group of the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool SetPrimaryGroup(  
   const CSid& rSid  
) throw(...);  
```  
  
#### Parameters  
 `rSid`  
 The [CSid Class](../vs140/CSid-Class.md) object containing the primary group information.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 The primary group is the default group for new objects created while this access token is in effect.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::GetPrimaryGroup](../vs140/CAccessToken--GetPrimaryGroup.md)