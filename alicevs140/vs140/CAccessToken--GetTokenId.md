---
title: "CAccessToken::GetTokenId"
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
ms.assetid: 74b03368-f720-4e15-8e0d-c7b6090f0cf8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetTokenId
Call this method to get the Token ID associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool GetTokenId(  
   LUID* pluid  
) const throw(...);  
```  
  
#### Parameters  
 `pluid`  
 Pointer to a [LUID](http://msdn.microsoft.com/library/windows/desktop/aa379261) which will receive the Token ID.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)