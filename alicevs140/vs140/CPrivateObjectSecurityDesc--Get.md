---
title: "CPrivateObjectSecurityDesc::Get"
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
ms.assetid: cbc6b6e7-79d8-4286-8d03-5cc911f07547
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrivateObjectSecurityDesc::Get
Call this method to retrieve information from a private object's security descriptor.  
  
## Syntax  
  
```  
  
      bool Get(  
   SECURITY_INFORMATION si,  
   CSecurityDesc* pResult   
) const throw( );  
```  
  
#### Parameters  
 `si`  
 A set of bit flags that indicate the parts of the security descriptor to retrieve. This value can be a combination of the [SECURITY_INFORMATION](http://msdn.microsoft.com/library/windows/desktop/aa379573) bit flags.  
  
 `pResult`  
 Pointer to a [CSecurityDesc](../vs140/CSecurityDesc-Class.md) object that receives a copy of the requested information from the specified security descriptor.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 The security descriptor is a structure and associated data that contains the security information for a securable object.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CPrivateObjectSecurityDesc Class](../vs140/CPrivateObjectSecurityDesc-Class.md)   
 [GetPrivateObjectSecurity](http://msdn.microsoft.com/library/windows/desktop/aa446646)   
 [CPrivateObjectSecurityDesc::Set](../vs140/CPrivateObjectSecurityDesc--Set.md)