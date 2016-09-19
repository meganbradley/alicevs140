---
title: "texture::operatorOperator"
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
ms.assetid: a71de53c-9da9-4086-b56d-53b1ac4461db
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# texture::operatorOperator
Returns the element that is at the specified index.  
  
## Syntax  
  
```  
const value_type operator[] (  
   const index<_Rank>& _Index  
) const restrict(amp);  
  
const value_type operator[] (  
   int _I0  
) const restrict(amp);  
```  
  
#### Parameters  
 `_Index`  
 The index.  
  
 `_I0`  
 The index.  
  
## Return Value  
 The element that is at the specified index.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [texture Class](../vs140/texture-Class.md)