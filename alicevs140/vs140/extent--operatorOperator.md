---
title: "extent::operatorOperator"
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
ms.topic: article
ms.assetid: b1aca19c-4add-4179-b3e1-6de26539a114
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# extent::operatorOperator
Returns the element that's at the specified index.  
  
## Syntax  
  
```  
int operator[] (  
   unsigned int _Index  
) const restrict(amp,cpu);  
  
int& operator[] (  
   unsigned int _Index  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Index`  
 An integer from 0 through the rank minus 1.  
  
## Return Value  
 The element that's at the specified index.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [extent Structure](../vs140/extent-Class--C---AMP-.md)