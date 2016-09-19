---
title: "texture::get Method"
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
ms.assetid: 78a2bfa3-8cfc-43ec-acb2-2140505849f1
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# texture::get Method
Returns the value of the element at the specified index.  
  
## Syntax  
  
```  
const value_type get(  
   const index<_Rank>& _Index  
) const restrict(amp);  
```  
  
#### Parameters  
 `_Index`  
 The index of the element.  
  
## Return Value  
 The value of the element at the specified index.  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [texture Class](../vs140/texture-Class.md)