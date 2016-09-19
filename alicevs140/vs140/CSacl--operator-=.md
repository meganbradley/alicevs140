---
title: "CSacl::operator ="
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
ms.assetid: 723294bd-ae39-4262-a5bf-f7c844201149
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSacl::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      CSacl & operator =(  
   const ACL & rhs   
) throw(...);  
```  
  
#### Parameters  
 `rhs`  
 The **ACL** (access-control list) to assign to the existing object.  
  
## Return Value  
 Returns a reference to the updated `CSacl` object. Ensure that the **ACL** parameter is actually a system access-control list (SACL) and not a discretionary access-control list (DACL). In debug builds an assertion will occur, and in release builds the **ACL** parameter will be ignored.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSacl Class](../vs140/CSacl-Class.md)