---
title: "CAccessToken::GetGroups"
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
ms.assetid: 803990b3-e6d6-47d1-9f3a-724ecb01655a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessToken::GetGroups
Call this method to return the `CAccessToken` object's token groups.  
  
## Syntax  
  
```  
  
      bool GetGroups(  
   CTokenGroups* pGroups  
) const throw(...);  
```  
  
#### Parameters  
 *pGroups*  
 Pointer to the [CTokenGroups Class](../vs140/CTokenGroups-Class.md) object which will receive the group information.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAccessToken Class](../vs140/CAccessToken-Class.md)