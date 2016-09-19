---
title: "CSimpleMapEqualHelper::IsEqualKey"
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
ms.assetid: 54a5448c-c9b9-43db-bc7c-794bbaa0d495
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMapEqualHelper::IsEqualKey
Tests two keys for equality.  
  
## Syntax  
  
```  
  
      static bool IsEqualKey(  
   const TKey& k1,  
   const TKey& k2   
);  
```  
  
#### Parameters  
 `k1`  
 The first key.  
  
 `k2`  
 The second key.  
  
## Return Value  
 Returns true if the keys are equal, false otherwise.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMapEqualHelper Class](../vs140/CSimpleMapEqualHelper-Class.md)   
 [CSimpleMapEqualHelper::IsEqualValue](../vs140/CSimpleMapEqualHelper--IsEqualValue.md)