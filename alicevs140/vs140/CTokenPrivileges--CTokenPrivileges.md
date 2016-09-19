---
title: "CTokenPrivileges::CTokenPrivileges"
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
ms.assetid: c9a1bd49-e3ed-431a-ac85-9fa9b8e41cd8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::CTokenPrivileges
The constructor.  
  
## Syntax  
  
```  
  
      CTokenPrivileges( ) throw( );   
CTokenPrivileges(  
   const CTokenPrivileges & rhs   
) throw(...);  
CTokenPrivileges(  
   const TOKEN_PRIVILEGES & rPrivileges  
) throw(...);  
```  
  
#### Parameters  
 `rhs`  
 The `CTokenPrivileges` object to assign to the new object.  
  
 `rPrivileges`  
 The [TOKEN_PRIVILEGES](http://msdn.microsoft.com/library/windows/desktop/aa379630) structure to assign to the new `CTokenPrivileges` object.  
  
## Remarks  
 The `CTokenPrivileges` object can optionally be created using a **TOKEN_PRIVILEGES** structure or a previously defined `CTokenPrivileges` object.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)   
 [CTokenPrivileges::~CTokenPrivileges](../vs140/CTokenPrivileges--~CTokenPrivileges.md)