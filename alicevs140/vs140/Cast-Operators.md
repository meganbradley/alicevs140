---
title: "Cast Operators"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 43b90bbd-39ef-43e6-ae5d-e8a67a01de40
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cast Operators
A type cast provides a method for explicit conversion of the type of an object in a specific situation.  
  
## Syntax  
 *cast-expression*:  
 *unary-expression*  
  
 **(**  *type-name*  **)**  *cast-expression*  
  
 The compiler treats *cast-expression* as type *type-name* after a type cast has been made. Casts can be used to convert objects of any scalar type to or from any other scalar type. Explicit type casts are constrained by the same rules that determine the effects of implicit conversions, discussed in [Assignment Conversions](../vs140/Assignment-Conversions.md). Additional restraints on casts may result from the actual sizes or representation of specific types. See [Storage of Basic Types](../vs140/Storage-of-Basic-Types.md) for information on actual sizes of integral types. For more information on type casts, see [Type-Cast Conversions](../vs140/Type-Cast-Conversions.md).  
  
## See Also  
 [Cast Operator: ()](../vs140/Cast-Operator----.md)