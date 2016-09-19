---
title: "CDacl::CDacl"
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
ms.assetid: f1b82dd9-2caa-4b24-8480-d9fcf4525ef4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDacl::CDacl
The constructor.  
  
## Syntax  
  
```  
  
      CDacl (  
   const ACL & rhs   
) throw(...);  
CDacl ( ) throw( );  
```  
  
#### Parameters  
 `rhs`  
 An existing **ACL** (access-control list) structure.  
  
## Remarks  
 The `CDacl` object can be optionally created using an existing **ACL** structure. It is important to note that only a DACL (discretionary access-control list), and not a SACL (system access-control list), should be passed as this parameter. In debug builds, passing a SACL will cause an ASSERT. In release builds, passing a SACL will cause the ACEs (access-control entries) in the ACL to be ignored, and no error will occur.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CDacl Class](../vs140/CDacl-Class.md)