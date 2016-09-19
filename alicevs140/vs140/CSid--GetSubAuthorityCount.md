---
title: "CSid::GetSubAuthorityCount"
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
ms.assetid: bfc9d1ec-ff61-40d9-b3f9-d1abf4dfb7a1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid::GetSubAuthorityCount
Returns the subauthority count.  
  
## Syntax  
  
```  
  
UCHAR GetSubAuthorityCount( ) const throw( );  
  
```  
  
## Return Value  
 If the method succeeds, the return value is the subauthority count.  
  
 If the method fails, the return value is undefined. The method fails if the `CSid` object is invalid. To get extended error information, call `GetLastError`.  
  
> [!NOTE]
>  Under debug builds the function will cause an ASSERT if the `CSid` object is not valid.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSid Class](../vs140/CSid-Class.md)   
 [CSid::GetSubAuthority](../vs140/CSid--GetSubAuthority.md)