---
title: "__based Grammar"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: a68ff750-c7fa-4c0c-8d5f-2df76e4686c5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __based Grammar
## Microsoft Specific  
 Based addressing is useful when you need precise control over the segment in which objects are allocated (static and dynamic based data).  
  
 The only form of based addressing acceptable in 32-bit and 64-bit compilations is "based on a pointer" that defines a type that contains a 32-bit or 64-bit displacement to a 32-bit or 64-bit base or based on `void`.  
  
## Grammar  
 *based-range-modifier*:  
 **__based(**  *base-expression*  **)**  
  
 *base-expression*:  
 *based-variablebased-abstract-declaratorsegment-namesegment-cast*  
  
 *based-variable*:  
 *identifier*  
  
 *based-abstract-declarator*:  
 *abstract-declarator*  
  
 *base-type*:  
 *type-name*  
  
## END Microsoft Specific  
  
## See Also  
 [Based Pointers](../vs140/Based-Pointers--C---.md)