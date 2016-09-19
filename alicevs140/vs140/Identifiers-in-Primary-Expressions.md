---
title: "Identifiers in Primary Expressions"
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
ms.assetid: d4602fe6-e7e6-40cc-9823-3b1ebf5d3d38
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Identifiers in Primary Expressions
Identifiers can have integral, **float**, `enum`, `struct`, **union**, array, pointer, or function type. An identifier is a primary expression provided it has been declared as designating an object (in which case it is an l-value) or as a function (in which case it is a function designator). See [L-Value and R-Value Expressions](../vs140/L-Value-and-R-Value-Expressions.md) for a definition of l-value.  
  
 The pointer value represented by an array identifier is not a variable, so an array identifier cannot form the left-hand operand of an assignment operation and therefore is not a modifiable l-value.  
  
 An identifier declared as a function represents a pointer whose value is the address of the function. The pointer addresses a function returning a value of a specified type. Thus, function identifiers also cannot be l-values in assignment operations. For more information, see [Identifiers](../vs140/C-Identifiers.md).  
  
## See Also  
 [C Primary Expressions](../vs140/C-Primary-Expressions.md)