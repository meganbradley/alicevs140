---
title: "CSecurityDesc::IsSaclProtected"
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
ms.assetid: c966d9c4-be36-4de7-8b16-1efe52ed0cfa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::IsSaclProtected
Determines if the system access-control list (SACL) is configured to prevent modifications.  
  
## Syntax  
  
```  
  
bool IsSaclProtected( ) const throw( );  
  
```  
  
## Return Value  
 Returns true if the SACL is configured to prevent the security descriptor from being modified by inheritable access-control entries (ACEs). Returns false otherwise.  
  
## Remarks  
 To set this flag, use the [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md) method.  
  
 This method is only meaningful for Windows 2000 or later, as only Windows 2000 supports automatic propagation of inheritable ACEs.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [SECURITY_DESCRIPTOR_CONTROL](http://msdn.microsoft.com/library/windows/desktop/aa379566)   
 [CSecurityDesc::IsSaclAutoInherited](../vs140/CSecurityDesc--IsSaclAutoInherited.md)   
 [CSecurityDesc::IsSaclDefaulted](../vs140/CSecurityDesc--IsSaclDefaulted.md)   
 [CSecurityDesc::IsSaclPresent](../vs140/CSecurityDesc--IsSaclPresent.md)