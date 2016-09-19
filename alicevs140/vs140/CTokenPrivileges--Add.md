---
title: "CTokenPrivileges::Add"
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
ms.assetid: 8b84c8e1-1ce1-4443-8e69-2341c3c6f4dd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::Add
Adds one or more privileges to the `CTokenPrivileges` access token object.  
  
## Syntax  
  
```  
  
      bool Add(  
   LPCTSTR pszPrivilege,  
   bool bEnable   
) throw(...);  
void Add(  
   const TOKEN_PRIVILEGES & rPrivileges   
) throw(...);  
```  
  
#### Parameters  
 `pszPrivilege`  
 Pointer to a null-terminated string that specifies the name of the privilege, as defined in the WINNT.H header file.  
  
 `bEnable`  
 If true, the privilege is enabled. If false, the privilege is disabled.  
  
 `rPrivileges`  
 Reference to a [TOKEN_PRIVILEGES](http://msdn.microsoft.com/library/windows/desktop/aa379630) structure. The privileges and attributes are copied from this structure and added to the `CTokenPrivileges` object.  
  
## Return Value  
 The first form of this method returns true if the privileges are successfully added, false otherwise.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)   
 [CTokenPrivileges::Delete](../vs140/CTokenPrivileges--Delete.md)   
 [CTokenPrivileges::DeleteAll](../vs140/CTokenPrivileges--DeleteAll.md)