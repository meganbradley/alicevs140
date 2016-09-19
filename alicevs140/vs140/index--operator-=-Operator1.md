---
title: "index::operator-= Operator1"
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
H1: index::operator-= Operator
ms.assetid: ee9f8b24-7309-4f1c-b845-4436d0d4f0ca
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# index::operator-= Operator1
Subtracts the specified number from each element of the [index](../vs140/index-Class.md) object.  
  
## Syntax  
  
```  
index<_Rank>& operator-=(  
   const index<_Rank>& _Rhs  
) restrict(amp,cpu);  
  
index<_Rank>& operator-=(  
   int _Rhs  
) restrict(amp,cpu);  
```  
  
#### Parameters  
 `_Rhs`  
 The number to subtract.  
  
## Return Value  
 The `index` object.  
  
## Requirements  
 **Header:** amp.h  
  
 **Namespace:** Concurrency  
  
## See Also  
 [index Structure](../vs140/index-Class.md)