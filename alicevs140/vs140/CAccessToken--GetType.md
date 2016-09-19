---
title: "CAccessToken::GetType"
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
ms.assetid: 0782bd8f-1546-487c-8b26-e63e2c51da6d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetType
Call this method to get the token type of the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool GetType(  
   TOKEN_TYPE* pType  
) const throw(...);  
```  
  
#### Parameters  
 `pType`  
 Address of the [TOKEN_TYPE](http://msdn.microsoft.com/library/windows/desktop/aa379633) variable that, on success, receives the type of the token.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 The **TOKEN_TYPE** enumeration type contains values that differentiate between a primary token and an impersonation token.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)