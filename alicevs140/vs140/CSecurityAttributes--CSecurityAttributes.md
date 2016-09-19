---
title: "CSecurityAttributes::CSecurityAttributes"
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
ms.assetid: b6321a35-1a42-492a-9c3e-b8e2e5b41ca7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityAttributes::CSecurityAttributes
The constructor.  
  
## Syntax  
  
```  
  
      CSecurityAttributes( ) throw( );   
explicit CSecurityAttributes(  
   const CSecurityDesc & rSecurityDescriptor,  
   bool bInheritsHandle = false  
) throw(...);  
```  
  
#### Parameters  
 `rSecurityDescriptor`  
 Reference to a security descriptor.  
  
 `bInheritsHandle`  
 Specifies whether the returned handle is inherited when a new process is created. If this member is true, the new process inherits the handle.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityAttributes Class](../vs140/CSecurityAttributes-Class.md)   
 [CSecurityAttributes::Set](../vs140/CSecurityAttributes--Set.md)