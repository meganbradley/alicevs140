---
title: "CSid::GetSubAuthority"
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
ms.assetid: 8d7da004-f037-4066-9537-b818662a2b7d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::GetSubAuthority
Returns a specified subauthority in a `SID` (security identifier) structure.  
  
## Syntax  
  
```  
  
      DWORD GetSubAuthority(  
   DWORD nSubAuthority   
) const throw( );  
```  
  
#### Parameters  
 *nSubAuthority*  
 The subauthority.  
  
## Return Value  
 Returns the subauthority referenced by *nSubAuthority.* The subauthority value is a relative identifier (RID).  
  
## Remarks  
 The *nSubAuthority* parameter specifies an index value identifying the subauthority array element the method will return. The method performs no validation tests on this value. An application can call [CSid::GetSubAuthorityCount](../vs140/CSid--GetSubAuthorityCount.md) to discover the range of acceptable values.  
  
> [!NOTE]
>  Under debug builds the function will cause an ASSERT if the `CSid` object is not valid.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)   
 [CSid::GetPSID_IDENTIFIER_AUTHORITY](../vs140/CSid--GetPSID_IDENTIFIER_AUTHORITY.md)