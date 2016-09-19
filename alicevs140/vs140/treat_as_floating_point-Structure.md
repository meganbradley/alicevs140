---
title: "treat_as_floating_point Structure"
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
ms.assetid: d0a2161c-bbb2-4924-8961-7568d5ad5434
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# treat_as_floating_point Structure
Specifies whether `Rep` can be treated as a floating-point type.  
  
## Syntax  
  
```  
template<class Rep>  
struct treat_as_floating_point : is_floating_point< Rep>;  
```  
  
## Remarks  
 `Rep` can be treated as a floating-point type only when the specialization `treat_as_floating_point<Rep>` is derived from [true_type](../vs140/-type_traits--typedefs.md#true_type_typedef). The template class can be specialized for a user-defined type.  
  
## Requirements  
 **Header:** chrono  
  
 **Namespace:** std::chrono  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<chrono\>](../vs140/-chrono-.md)