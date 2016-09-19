---
title: "CSecurityDesc::MakeAbsolute"
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
ms.assetid: 4b1bcb2b-5392-41d9-823c-e5a2912ad950
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::MakeAbsolute
Call this method to convert the security descriptor to absolute format.  
  
## Syntax  
  
```  
  
bool MakeAbsolute( ) throw(...);  
  
```  
  
## Return Value  
 Returns true if the method succeeds, false otherwise.  
  
## Remarks  
 A security descriptor in absolute format contains pointers to the information it contains, rather than the information itself. A security descriptor in self-relative format contains the information in a contiguous block of memory. In a self-relative security descriptor, a **SECURITY_DESCRIPTOR** structure always starts the information, but the security descriptor's other components can follow the structure in any order. Instead of using memory addresses, the components of the self-relative security descriptor are identified by offsets from the beginning of the security descriptor. This format is useful when a security descriptor must be stored on a disk or transmitted by means of a communications protocol. For more information, see [Absolute and Self-Relative Security Descriptors](http://msdn.microsoft.com/library/windows/desktop/aa374807).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [SECURITY_DESCRIPTOR_CONTROL](http://msdn.microsoft.com/library/windows/desktop/aa379566)   
 [Absolute and Self-Relative Security Descriptors](http://msdn.microsoft.com/library/windows/desktop/aa374807)   
 [CSecurityDesc::MakeSelfRelative](../vs140/CSecurityDesc--MakeSelfRelative.md)   
 [CSecurityDesc::IsSelfRelative](../vs140/CSecurityDesc--IsSelfRelative.md)   
 [MakeAbsoluteSD](http://msdn.microsoft.com/library/windows/desktop/aa379264)