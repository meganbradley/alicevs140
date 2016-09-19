---
title: "Casting Operators"
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
ms.topic: index-page 
ms.assetid: 16240348-26bc-4f77-8eab-57253f00ce52
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Casting Operators
There are several casting operators specific to the C++ language. These operators are intended to remove some of the ambiguity and danger inherent in old style C language casts. These operators are:  
  
-   [dynamic_cast](../vs140/dynamic_cast-Operator.md) Used for conversion of polymorphic types.  
  
-   [static_cast](../vs140/static_cast-Operator.md) Used for conversion of nonpolymorphic types.  
  
-   [const_cast](../vs140/const_cast-Operator.md) Used to remove the `const`, `volatile`, and `__unaligned` attributes.  
  
-   [reinterpret_cast](../vs140/reinterpret_cast-Operator.md) Used for simple reinterpretation of bits.  
  
-   [safe_cast](../vs140/safe_cast--C---Component-Extensions-.md) Used to produce verifiable MSIL.  
  
 Use `const_cast` and `reinterpret_cast` as a last resort, since these operators present the same dangers as old style casts. However, they are still necessary in order to completely replace old style casts.  
  
## See Also  
 [Casting](../vs140/Casting.md)