---
title: "CAccessToken::PrivilegeCheck"
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
ms.assetid: 9c6d4fbe-3936-4dba-813d-6c544fdecb8a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::PrivilegeCheck
Call this method to determine whether a specified set of privileges are enabled in the **CAccessToken** object.  
  
## Syntax  
  
```  
  
      bool PrivilegeCheck(  
   PPRIVILEGE_SET RequiredPrivileges,  
   bool* pbResult   
) const throw( );  
```  
  
#### Parameters  
 *RequiredPrivileges*  
 Pointer to a [PRIVILEGE_SET](http://msdn.microsoft.com/library/windows/desktop/aa379307) structure.  
  
 *pbResult*  
 Pointer to a value the method sets to indicate whether any or all of the specified privilege are enabled in the `CAccessToken` object.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 When `PrivilegeCheck` returns, the **Attributes** member of each [LUID_AND_ATTRIBUTES](http://msdn.microsoft.com/library/windows/desktop/aa379263) structure is set to SE_PRIVILEGE_USED_FOR_ACCESS if the corresponding privilege is enabled. This method calls the [PrivilegeCheck](http://msdn.microsoft.com/library/windows/desktop/aa379304) Win32 function.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)