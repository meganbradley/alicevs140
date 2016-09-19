---
title: "CAccessToken::GetLogonSessionId"
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
ms.assetid: b09395b7-a734-45d2-be83-f7fcf2ca82ec
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetLogonSessionId
Call this method to get the Logon Session ID associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool GetLogonSessionId(  
   LUID* pluid  
) const throw(...);  
```  
  
#### Parameters  
 `pluid`  
 Pointer to a [LUID](http://msdn.microsoft.com/library/windows/desktop/aa379261) which will receive the Logon Session ID.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 In debug builds, an assertion error will occur if `pluid` is an invalid value.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)