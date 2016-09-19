---
title: "CSid::AccountName"
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
ms.assetid: 6add86a8-bb1c-4910-91ee-b50039e86692
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::AccountName
Returns the name of the account associated with the `CSid` object.  
  
## Syntax  
  
```  
  
LPCTSTR AccountName( ) const throw(...);  
  
```  
  
## Return Value  
 Returns the `LPCTSTR` pointing to the name of the account.  
  
## Remarks  
 This method attempts to find a name for the specified `SID` (security identifier). For full details, see [LookupAccountSid](http://msdn.microsoft.com/library/windows/desktop/aa379166).  
  
 If no account name for the `SID` can be found, `AccountName` returns an empty string. This can occur if a network timeout prevents this method from finding the name. It also occurs for security identifiers with no corresponding account name, such as a logon `SID` that identifies a logon session.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)   
 [CSid::Domain](../vs140/CSid--Domain.md)   
 [LookupAccountSid](http://msdn.microsoft.com/library/windows/desktop/aa379166)