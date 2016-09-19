---
title: "CSecurityDesc::GetGroup"
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
ms.assetid: b0d86007-7dae-40e8-b11e-b05578452021
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::GetGroup
Retrieves the primary group information from the security descriptor.  
  
## Syntax  
  
```  
  
      bool GetGroup(  
   CSid * pSid,  
   bool * pbDefaulted = NULL   
) const throw(...);  
```  
  
#### Parameters  
 `pSid`  
 Pointer to a [CSid](../vs140/CSid-Class.md) (security identifier) that receives a copy of the group stored in the CDacl.  
  
 `pbDefaulted`  
 Pointer to a flag set to the value of the SE_GROUP_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure when the method returns.  
  
## Return Value  
 Returns true if the method succeeds, false if it fails.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [GetSecurityDescriptorGroup](http://msdn.microsoft.com/library/windows/desktop/aa446649)   
 [CSecurityDesc::GetControl](../vs140/CSecurityDesc--GetControl.md)   
 [CSecurityDesc::GetDacl](../vs140/CSecurityDesc--GetDacl.md)   
 [CSecurityDesc::GetOwner](../vs140/CSecurityDesc--GetOwner.md)   
 [CSecurityDesc::GetSacl](../vs140/CSecurityDesc--GetSacl.md)   
 [CSecurityDesc::SetGroup](../vs140/CSecurityDesc--SetGroup.md)