---
title: "CSimpleMap::FindVal"
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
ms.assetid: bd1073aa-6be1-4599-af59-ca0b927d6cc2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMap::FindVal
Finds a specific value.  
  
## Syntax  
  
```  
  
      int FindVal(  
   const TVal& val   
) const;  
```  
  
#### Parameters  
 *val*  
 The value for which to search.  
  
## Return Value  
 Returns the index of the value if it is found, otherwise returns -1.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMap Class](../vs140/CSimpleMap-Class.md)   
 [CSimpleMap::FindKey](../vs140/CSimpleMap--FindKey.md)