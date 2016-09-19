---
title: "Type-Cast Conversions"
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
ms.assetid: 57ab5902-f12f-4326-a2f6-6282f1d4025a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type-Cast Conversions
You can use type casts to explicitly convert types.  
  
 **Syntax**  
  
 *cast-expression*:  
 *unary expression*  
  
 **(**  *type-name*  **)**  *cast-expression*  
  
 *type-name*:  
 *specifier-qualifier-list abstract-declarator* opt  
  
 The *type-name* is a type and *cast-expression* is a value to be converted to that type. An expression with a type cast is not an l-value. The *cast-expression* is converted as though it had been assigned to a variable of type *type-name*. The conversion rules for assignments (outlined in [Assignment Conversions](../vs140/Assignment-Conversions.md)) apply to type casts as well. The following table shows the types that can be cast to any given type.  
  
### Legal Type Casts  
  
|Destination Types|Potential Sources|  
|-----------------------|-----------------------|  
|Integral types|Any integer type or floating-point type, or pointer to an object|  
|Floating-point|Any arithmetic type|  
|A pointer to an object, or (**void \***)|Any integer type, (**void \***), a pointer to an object, or a function pointer|  
|Function pointer|Any integral type, a pointer to an object, or a function pointer|  
|A structure, union, or array|None|  
|Void type|Any type|  
  
 Any identifier can be cast to `void` type. However, if the type specified in a type-cast expression is not `void`, then the identifier being cast to that type cannot be a `void` expression. Any expression can be cast to `void`, but an expression of type `void` cannot be cast to any other type. For example, a function with `void` return type cannot have its return cast to another type.  
  
 Note that a **void \*** expression has a type pointer to `void`, not type `void`. If an object is cast to `void` type, the resulting expression cannot be assigned to any item. Similarly, a type-cast object is not an acceptable l-value, so no assignment can be made to a type-cast object.  
  
 **Microsoft Specific**  
  
 A type cast can be an l-value expression as long as the size of the identifier does not change. For information on l-value expressions, see [L-Value and R-Value Expressions](../vs140/L-Value-and-R-Value-Expressions.md).  
  
 **END Microsoft Specific**  
  
 You can convert an expression to type `void` with a cast, but the resulting expression can be used only where a value is not required. An object pointer converted to **void \*** and back to the original type will return to its original value.  
  
## See Also  
 [Type Conversions (C)](../vs140/Type-Conversions--C-.md)