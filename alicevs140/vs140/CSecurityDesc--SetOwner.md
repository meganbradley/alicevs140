---
title: "CSecurityDesc::SetOwner"
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
ms.assetid: e3b66091-3a91-499b-9c94-ad78d99126e6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::SetOwner
Sets the owner information of an absolute format security descriptor. It replaces any owner information already present.  
  
## Syntax  
  
```  
  
      bool SetOwner(  
   const CSid & Sid,  
   bool bDefaulted = false   
) throw(...);  
```  
  
#### Parameters  
 `Sid`  
 The [CSid](../vs140/CSid-Class.md) object for the security descriptor's new primary owner. This parameter must not be NULL.  
  
 `bDefaulted`  
 Indicates whether the owner information is derived from a default mechanism. If this value is true, it is default information. The method stores this value as the SE_OWNER_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure. If this parameter is zero, the SE_OWNER_DEFAULTED flag is cleared.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [CSecurityDesc::SetControl](../vs140/CSecurityDesc--SetControl.md)   
 [CSecurityDesc::SetGroup](../vs140/CSecurityDesc--SetGroup.md)   
 [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md)   
 [CSecurityDesc::GetOwner](../vs140/CSecurityDesc--GetOwner.md)