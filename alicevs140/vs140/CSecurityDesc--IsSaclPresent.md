---
title: "CSecurityDesc::IsSaclPresent"
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
ms.assetid: ce01b9e2-d6de-4fb2-8701-cc96ed6c3d41
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::IsSaclPresent
Determines if the security descriptor contains a system access-control list (SACL).  
  
## Syntax  
  
```  
  
bool IsSaclPresent( ) const throw( );  
  
```  
  
## Return Value  
 Returns true if the security descriptor contains a SACL, false otherwise.  
  
## Remarks  
 To set this flag, use the [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md) method.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [SECURITY_DESCRIPTOR_CONTROL](http://msdn.microsoft.com/library/windows/desktop/aa379566)   
 [CSecurityDesc::IsSaclAutoInherited](../vs140/CSecurityDesc--IsSaclAutoInherited.md)   
 [CSecurityDesc::IsSaclDefaulted](../vs140/CSecurityDesc--IsSaclDefaulted.md)   
 [CSecurityDesc::IsSaclProtected](../vs140/CSecurityDesc--IsSaclProtected.md)