---
title: "CTokenPrivileges::GetLength"
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
ms.assetid: 33651c5b-0789-43bc-b06d-c6b5396c375d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::GetLength
Returns the length of the `CTokenPrivileges` object.  
  
## Syntax  
  
```  
  
UINT GetLength( ) const throw( );  
  
```  
  
## Return Value  
 Returns the number of bytes required to hold a **TOKEN_PRIVILEGES** structure represented by the `CTokenPrivileges` object, including all of the privilege entries it contains.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)   
 [CTokenPrivileges::GetCount](../vs140/CTokenPrivileges--GetCount.md)