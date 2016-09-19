---
title: "CAccessToken::DisablePrivileges"
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
ms.assetid: 8cffe2ac-3973-42c1-b2f3-f44c80f7a21c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::DisablePrivileges
Call this method to disable one or more privileges in the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool DisablePrivileges(  
   const CAtlArray< LPCTSTR >& rPrivileges,  
   CTokenPrivileges* pPreviousState = NULL  
) throw(...);  
```  
  
#### Parameters  
 `rPrivileges`  
 Pointer to an array of strings containing the privileges to disable in the `CAccessToken` object.  
  
 `pPreviousState`  
 Pointer to a `CTokenPrivileges` object which will contain the previous state of the privileges.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::DisablePrivilege](../vs140/CAccessToken--DisablePrivilege.md)   
 [CAccessToken::EnablePrivileges](../vs140/CAccessToken--EnablePrivileges.md)