---
title: "CTokenPrivileges::GetPTOKEN_PRIVILEGES"
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
ms.assetid: be530218-45b6-4812-bfac-61e4ba9b75e8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::GetPTOKEN_PRIVILEGES
Returns a pointer to the **TOKEN_PRIVILEGES** structure.  
  
## Syntax  
  
```  
  
const TOKEN_PRIVILEGES * GetPTOKEN_PRIVILEGES( ) const throw(...);  
  
```  
  
## Return Value  
 Returns a pointer to the [TOKEN_PRIVILEGES](http://msdn.microsoft.com/library/windows/desktop/aa379630) structure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)   
 [TOKEN_PRIVILEGES](http://msdn.microsoft.com/library/windows/desktop/aa379630)