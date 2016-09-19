---
title: "CSecurityDesc::IsDaclDefaulted"
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
ms.assetid: 35a058e8-9a65-479b-bf34-113b10664a22
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::IsDaclDefaulted
Determines if the security descriptor is configured with a default discretionary access-control list (DACL).  
  
## Syntax  
  
```  
  
bool IsDaclDefaulted( ) const throw( );  
  
```  
  
## Return Value  
 Returns true if the security descriptor contains a default DACL, false otherwise.  
  
## Remarks  
 This flag can affect how the system treats the DACL, with respect to access-control entry (ACE) inheritance. For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token. The system ignores this flag if the SE_DACL_PRESENT flag is not set.  
  
 This flag is used to determine how the final DACL on the object is to be computed and is not stored physically in the security descriptor control of the securable object.  
  
 To set this flag, use the [CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md) method.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [SECURITY_DESCRIPTOR_CONTROL](http://msdn.microsoft.com/library/windows/desktop/aa379566)   
 [CSecurityDesc::IsDaclAutoInherited](../vs140/CSecurityDesc--IsDaclAutoInherited.md)   
 [CSecurityDesc::IsDaclPresent](../vs140/CSecurityDesc--IsDaclPresent.md)   
 [CSecurityDesc::IsDaclProtected](../vs140/CSecurityDesc--IsDaclProtected.md)