---
title: "CAccessToken::EnablePrivileges"
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
ms.assetid: 8d5ca12e-b704-45f6-881d-1884dfd02a51
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::EnablePrivileges
Call this method to enable one or more privileges in the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool EnablePrivileges(  
   const CAtlArray< LPCTSTR >& rPrivileges,  
   CTokenPrivileges* pPreviousState = NULL  
) throw(...);  
```  
  
#### Parameters  
 `rPrivileges`  
 Pointer to an array of strings containing the privileges to enable in the `CAccessToken` object.  
  
 `pPreviousState`  
 Pointer to a `CTokenPrivileges` object which will contain the previous state of the privileges.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::EnablePrivilege](../vs140/CAccessToken--EnablePrivilege.md)   
 [CAccessToken::DisablePrivileges](../vs140/CAccessToken--DisablePrivileges.md)