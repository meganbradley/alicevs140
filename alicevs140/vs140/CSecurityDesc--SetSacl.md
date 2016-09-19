---
title: "CSecurityDesc::SetSacl"
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
ms.assetid: 019173fc-f961-428d-95ac-353eb0fabec2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::SetSacl
Sets information in a system access-control list (SACL). If a SACL is already present in the security descriptor, it is replaced.  
  
## Syntax  
  
```  
  
      bool SetSacl(  
   const CSacl & Sacl,  
   bool bDefaulted = false   
) throw(...);  
```  
  
#### Parameters  
 *Sacl*  
 Pointer to an `CSacl` object specifying the SACL for the security descriptor. This parameter must not be NULL, and must be a CSacl object. Unlike DACLs, there is no difference between NULL and an empty SACL, as SACL objects do not specify access rights, only auditing information.  
  
 `bDefaulted`  
 Specifies a flag indicating the source of the SACL. If this flag is true, the SACL has been retrieved by some default mechanism. If false, the SACL has been explicitly specified by a user. The method stores this value in the SE_SACL_DEFAULTED flag of the **SECURITY_DESCRIPTOR_CONTROL** structure. If this parameter is not specified, the SE_SACL_DEFAULTED flag is cleared.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [CSecurityDesc::SetControl](../vs140/CSecurityDesc--SetControl.md)   
 [CSecurityDesc::SetGroup](../vs140/CSecurityDesc--SetGroup.md)   
 [CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md)   
 [CSecurityDesc::SetOwner](../vs140/CSecurityDesc--SetOwner.md)   
 [CSecurityDesc::GetSacl](../vs140/CSecurityDesc--GetSacl.md)