---
title: "CAccessToken::LogonUser"
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
ms.assetid: 967680e0-934b-4586-b2ee-975745f5af68
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::LogonUser
Call this method to create a logon session for the user associated with the given credentials.  
  
## Syntax  
  
```  
  
      bool LogonUser(  
   LPCTSTR pszUserName,  
   LPCTSTR pszDomain,  
   LPCTSTR pszPassword,  
   DWORD dwLogonType = LOGON32_LOGON_INTERACTIVE,  
   DWORD dwLogonProvider = LOGON32_PROVIDER_DEFAULT   
) throw( );  
```  
  
#### Parameters  
 `pszUserName`  
 Pointer to a null-terminated string that specifies the user name. This is the name of the user account to log on to.  
  
 *pszDomain*  
 Pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the `pszUserName` account.  
  
 `pszPassword`  
 Pointer to a null-terminated string that specifies the clear-text password for the user account specified by `pszUserName`.  
  
 *dwLogonType*  
 Specifies the type of logon operation to perform. See [LogonUser](http://msdn.microsoft.com/library/windows/desktop/aa378184) for more details.  
  
 *dwLogonProvider*  
 Specifies the logon provider. See [LogonUser](http://msdn.microsoft.com/library/windows/desktop/aa378184) for more details.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 The access token resulting from the logon will be associated with the `CAccessToken`. For this method to succeed, the `CAccessToken` object must hold SE_TCB_NAME privileges, identifying the holder as part of the trusted computer base. See [LogonUser](http://msdn.microsoft.com/library/windows/desktop/aa378184) for more information regarding the privileges required.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::ImpersonateLoggedOnUser](../vs140/CAccessToken--ImpersonateLoggedOnUser.md)