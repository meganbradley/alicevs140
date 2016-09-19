---
title: "CAccessToken::GetStatistics"
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
ms.assetid: 2812d8f8-af12-43b7-819d-ca0484dcef05
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetStatistics
Call this method to get information associated with the `CAccessToken` object.  
  
## Syntax  
  
```  
  
      bool GetStatistics(  
   TOKEN_STATISTICS* pStatistics  
) const throw(...);  
```  
  
#### Parameters  
 *pStatistics*  
 Pointer to a [TOKEN_STATISTICS](http://msdn.microsoft.com/library/windows/desktop/aa379632) structure.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)