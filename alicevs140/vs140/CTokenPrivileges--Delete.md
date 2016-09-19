---
title: "CTokenPrivileges::Delete"
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
ms.assetid: 99dc761f-72e3-4f66-b321-68a258b82733
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::Delete
Deletes a privilege from the `CTokenPrivileges` access token object.  
  
## Syntax  
  
```  
  
      bool Delete(  
   LPCTSTR pszPrivilege   
) throw( );  
```  
  
#### Parameters  
 `pszPrivilege`  
 Pointer to a null-terminated string that specifies the name of the privilege, as defined in the WINNT.H header file. For example, this parameter could specify the constant SE_SECURITY_NAME, or its corresponding string, "SeSecurityPrivilege."  
  
## Return Value  
 Returns true if the privilege was successfully deleted, false otherwise.  
  
## Remarks  
 This method is useful as a tool for creating restricted tokens under Windows 2000.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)   
 [CTokenPrivileges::DeleteAll](../vs140/CTokenPrivileges--DeleteAll.md)   
 [CTokenPrivileges::Add](../vs140/CTokenPrivileges--Add.md)   
 [CAccessToken::CreateRestrictedToken](../vs140/CAccessToken--CreateRestrictedToken.md)