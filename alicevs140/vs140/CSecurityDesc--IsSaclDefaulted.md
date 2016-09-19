---
title: "CSecurityDesc::IsSaclDefaulted"
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
ms.assetid: db20e0f0-0a8f-45eb-9e9a-c46f3c135a55
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::IsSaclDefaulted
Determines if the security descriptor is configured with a default system access-control list (SACL).  
  
## Syntax  
  
```  
  
bool IsSaclDefaulted( ) const throw( );  
  
```  
  
## Return Value  
 Returns true if the security descriptor contains a default SACL, false otherwise.  
  
## Remarks  
 This flag can affect how the system treats the SACL, with respect to access-control entry (ACE) inheritance. The system ignores this flag if the SE_SACL_PRESENT flag is not set.  
  
 To set this flag, use the [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md) method.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [SECURITY_DESCRIPTOR_CONTROL](http://msdn.microsoft.com/library/windows/desktop/aa379566)   
 [CSecurityDesc::IsSaclAutoInherited](../vs140/CSecurityDesc--IsSaclAutoInherited.md)   
 [CSecurityDesc::IsSaclPresent](../vs140/CSecurityDesc--IsSaclPresent.md)   
 [CSecurityDesc::IsSaclProtected](../vs140/CSecurityDesc--IsSaclProtected.md)