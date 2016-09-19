---
title: "CSid::GetPSID_IDENTIFIER_AUTHORITY"
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
ms.assetid: 3005a503-1afe-404d-abdb-d0ff5be9fc83
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::GetPSID_IDENTIFIER_AUTHORITY
Returns a pointer to the **SID_IDENTIFIER_AUTHORITY** structure.  
  
## Syntax  
  
```  
  
const SID_IDENTIFIER_AUTHORITY * GetPSID_IDENTIFIER_AUTHORITY( ) const throw();  
  
```  
  
## Return Value  
 If the method succeeds, it returns the address of the **SID_IDENTIFIER_AUTHORITY** structure. If it fails, the return value is undefined. Failure may occur if the `CSid` object is not valid, in which case the [CSid::IsValid](../vs140/CSid--IsValid.md) method returns **false**. The function `GetLastError` can be called for extended error information.  
  
> [!NOTE]
>  Under debug builds the function will cause an ASSERT if the `CSid` object is not valid.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)   
 [CSid::GetSubAuthority](../vs140/CSid--GetSubAuthority.md)