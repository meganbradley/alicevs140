---
title: "CTokenPrivileges::LookupPrivilege"
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
ms.assetid: e799456a-b7b2-4fa3-a591-8f2200c9061e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::LookupPrivilege
Retrieves the attribute associated with a given privilege name.  
  
## Syntax  
  
```  
  
      bool LookupPrivilege(  
   LPCTSTR pszPrivilege,  
   DWORD * pdwAttributes = NULL   
) const throw(...);  
```  
  
#### Parameters  
 `pszPrivilege`  
 Pointer to a null-terminated string that specifies the name of the privilege, as defined in the WINNT.H header file. For example, this parameter could specify the constant SE_SECURITY_NAME, or its corresponding string, "SeSecurityPrivilege."  
  
 `pdwAttributes`  
 Pointer to a variable that receives the attributes.  
  
## Return Value  
 Returns true if the attribute is successfully retrieved, false otherwise.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)   
 [CTokenPrivileges::GetNamesAndAttributes](../vs140/CTokenPrivileges--GetNamesAndAttributes.md)   
 [CTokenPrivileges::GetDisplayNames](../vs140/CTokenPrivileges--GetDisplayNames.md)   
 [CTokenPrivileges::GetLuidsAndAttributes](../vs140/CTokenPrivileges--GetLuidsAndAttributes.md)