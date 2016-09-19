---
title: "CSecurityDesc::GetControl"
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
ms.assetid: ba51e09b-4c17-4f5f-8230-a7edbd218605
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::GetControl
Retrieves control information from the security descriptor.  
  
## Syntax  
  
```  
  
      bool GetControl(  
   SECURITY_DESCRIPTOR_CONTROL * psdc   
) const throw( );  
```  
  
#### Parameters  
 *psdc*  
 Pointer to a **SECURITY_DESCRIPTOR_CONTROL** structure that receives the security descriptor's control information.  
  
## Return Value  
 Returns true if the method succeeds, false if it fails.  
  
## Remarks  
 This method is only meaningful when using Windows 2000 or later, as it calls [GetSecurityDescriptorControl](http://msdn.microsoft.com/library/windows/desktop/aa446647).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [CSecurityDesc::GetDacl](../vs140/CSecurityDesc--GetDacl.md)   
 [CSecurityDesc::GetGroup](../vs140/CSecurityDesc--GetGroup.md)   
 [CSecurityDesc::GetOwner](../vs140/CSecurityDesc--GetOwner.md)   
 [CSecurityDesc::GetSacl](../vs140/CSecurityDesc--GetSacl.md)   
 [CSecurityDesc::SetControl](../vs140/CSecurityDesc--SetControl.md)