---
title: "CAccessToken::IsTokenRestricted"
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
ms.assetid: 3e0ffd55-0f98-46f2-aeec-647b52c2114e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::IsTokenRestricted
Call this method to test if the `CAccessToken` object contains a list of restricted SIDs.  
  
## Syntax  
  
```  
  
bool IsTokenRestricted( ) const throw( );  
  
```  
  
## Return Value  
 Returns true if the object contains a list of restricting SIDs, false if there are no restricting SIDs or if the method fails.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)