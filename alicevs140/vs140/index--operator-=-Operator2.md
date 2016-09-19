---
title: "index::operator-= Operator2"
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
H1: index::operator/= Operator
ms.assetid: 48191629-07ee-45cc-b4de-ba48acacbe9a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# index::operator-= Operator2
Divides each element in the [index](../vs140/index-Class.md) object by the specified number.  
  
## Syntax  
  
```  
index<_Rank>& operator/=(  
   int _Rhs  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Rhs`  
 The number to divide by.  
  
## Return Value  
 The `index` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [index Structure](../vs140/index-Class.md)