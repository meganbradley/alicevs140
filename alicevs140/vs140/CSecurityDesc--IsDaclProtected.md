---
title: "CSecurityDesc::IsDaclProtected"
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
ms.assetid: dfe565fc-7116-4aa3-bf59-895ed1259bd9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::IsDaclProtected
Determines if the discretionary access-control list (DACL) is configured to prevent modifications.  
  
## Syntax  
  
```  
  
bool IsDaclProtected( ) const throw( );  
  
```  
  
## Return Value  
 Returns true if the DACL is configured to prevent the security descriptor from being modified by inheritable access-control entries (ACEs). Returns false otherwise.  
  
## Remarks  
 To set this flag, use the [CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md) method.  
  
 This method is only meaningful for Windows 2000 or later, as only Windows 2000 supports automatic propagation of inheritable ACEs.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [SECURITY_DESCRIPTOR_CONTROL](http://msdn.microsoft.com/library/windows/desktop/aa379566)   
 [CSecurityDesc::IsDaclAutoInherited](../vs140/CSecurityDesc--IsDaclAutoInherited.md)   
 [CSecurityDesc::IsDaclDefaulted](../vs140/CSecurityDesc--IsDaclDefaulted.md)   
 [CSecurityDesc::IsDaclPresent](../vs140/CSecurityDesc--IsDaclPresent.md)