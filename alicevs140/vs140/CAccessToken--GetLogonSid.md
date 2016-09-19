---
title: "CAccessToken::GetLogonSid"
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
ms.assetid: 5984b862-1e04-4c06-a33a-0ddd4e6fd901
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetLogonSid
Call this method to get the Logon SID associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool GetLogonSid(  
   CSid* pSid  
) const throw(...);  
```  
  
#### Parameters  
 `pSid`  
 Pointer to a [CSid Class](../vs140/CSid-Class.md) object.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 In debug builds, an assertion error will occur if *pSid* is an invalid value.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)