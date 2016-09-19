---
title: "CAccessToken::Attach"
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
ms.assetid: 440fcf21-6751-4b5d-b3a8-5c68b3bcaff1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::Attach
Call this method to take ownership of the given access token handle.  
  
## Syntax  
  
```  
  
      void Attach(  
   HANDLE hToken  
) throw( );  
```  
  
#### Parameters  
 *hToken*  
 A handle to the access token.  
  
## Remarks  
 In debug builds, an assertion error will occur if the `CAccessToken` object already has ownership of an access token.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)   
 [CAccessToken::Detach](../vs140/CAccessToken--Detach.md)