---
title: "CSecurityDesc::GetPSECURITY_DESCRIPTOR"
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
ms.assetid: 72db05d4-afa9-423b-af19-f9a93810066f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::GetPSECURITY_DESCRIPTOR
Returns a pointer to the **SECURITY_DESCRIPTOR** structure.  
  
## Syntax  
  
```  
  
const SECURITY_DESCRIPTOR * GetPSECURITY_DESCRIPTOR( ) const throw( );  
  
```  
  
## Return Value  
 Returns a pointer to the [SECURITY_DESCRIPTOR](http://msdn.microsoft.com/library/windows/desktop/aa379561) structure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [SECURITY_DESCRIPTOR](http://msdn.microsoft.com/library/windows/desktop/aa379561)