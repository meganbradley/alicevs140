---
title: "CTokenPrivileges::operator ="
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
ms.assetid: 708dfef4-a07f-46d2-a028-374e2a3afa01
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::operator =
Assignment operator.  
  
## Syntax  
  
```  
  
      CTokenPrivileges & operator =(  
   const TOKEN_PRIVILEGES & rPrivileges  
) throw(...);  
CTokenPrivileges & operator =(  
   const CTokenPrivileges & rhs   
) throw(...);  
```  
  
#### Parameters  
 `rPrivileges`  
 The [TOKEN_PRIVILEGES](http://msdn.microsoft.com/library/windows/desktop/aa379630) structure to assign to the `CTokenPrivileges` object.  
  
 `rhs`  
 The `CTokenPrivileges` object to assign to the object.  
  
## Return Value  
 Returns the updated `CTokenPrivileges` object.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)