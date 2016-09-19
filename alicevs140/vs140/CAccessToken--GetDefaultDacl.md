---
title: "CAccessToken::GetDefaultDacl"
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
ms.assetid: c6df3410-427a-4228-bfcc-6d9c7cd2999c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetDefaultDacl
Call this method to return the `CAccessToken` object's default DACL.  
  
## Syntax  
  
```  
  
      bool GetDefaultDacl(  
   CDacl* pDacl  
) const throw(...);  
```  
  
#### Parameters  
 `pDacl`  
 Pointer to the [CDacl Class](../vs140/CDacl-Class.md) object which will receive the **CAccessToken** object's default DACL.  
  
## Return Value  
 Returns true if the default DACL has been recovered, false otherwise.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::SetDefaultDacl](../vs140/CAccessToken--SetDefaultDacl.md)