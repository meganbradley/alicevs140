---
title: "CAccessToken::GetTerminalServicesSessionId"
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
ms.assetid: 90a5833c-e9f9-4691-9c41-dc322e63ffb3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetTerminalServicesSessionId
Call this method to get the Terminal Services Session ID associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool GetTerminalServicesSessionId(  
   DWORD* pdwSessionId  
) const throw(...);  
```  
  
#### Parameters  
 *pdwSessionId*  
 The Terminal Services Session ID.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)