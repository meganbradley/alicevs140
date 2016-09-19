---
title: "CSimpleMapEqualHelperFalse::IsEqualKey"
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
ms.assetid: a31369a0-f92e-4554-9b06-9713cf7eb708
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMapEqualHelperFalse::IsEqualKey
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
  
## Remarks  
 This method calls [CSimpleArrayEqualHelper](../vs140/CSimpleArrayEqualHelper-Class.md).  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMapEqualHelperFalse Class](../vs140/CSimpleMapEqualHelperFalse-Class.md)   
 [CSimpleMapEqualHelperFalse::IsEqualValue](../vs140/CSimpleMapEqualHelperFalse--IsEqualValue.md)