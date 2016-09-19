---
title: "CAccessToken::SetOwner"
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
ms.assetid: 339d4b26-5476-4664-a832-37843d3c2de1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::SetOwner
Call this method to set the owner of the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool SetOwner(  
   const CSid& rSid  
) throw(...);  
```  
  
#### Parameters  
 `rSid`  
 The [CSid Class](../vs140/CSid-Class.md) object containing the owner information.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 The owner is the default owner that is used for new objects created while this access token is in effect.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::GetOwner](../vs140/CAccessToken--GetOwner.md)