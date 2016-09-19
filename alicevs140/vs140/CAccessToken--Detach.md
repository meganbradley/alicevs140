---
title: "CAccessToken::Detach"
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
ms.assetid: 189d9dea-8e94-41de-8d1b-e172f867111c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::Detach
Call this method to revoke ownership of the access token.  
  
## Syntax  
  
```  
  
HANDLE Detach( ) throw( );  
  
```  
  
## Return Value  
 Returns the handle to the `CAccessToken` which has been detached.  
  
## Remarks  
 This method revokes the `CAccessToken`'s ownership of the access token.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::Attach](../vs140/CAccessToken--Attach.md)