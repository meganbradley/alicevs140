---
title: "Logical Negation Operator: !"
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
ms.topic: language-reference
ms.assetid: 650add9f-a7bc-426c-b01d-5fc6a81c8b62
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Logical Negation Operator: !
## Syntax  
  
```  
  
! cast-expression  
```  
  
## Remarks  
 The logical negation operator (**!**) reverses the meaning of its operand. The operand must be of arithmetic or pointer type (or an expression that evaluates to arithmetic or pointer type). The operand is implicitly converted to type `bool`. The result is **true** if the converted operand is **false**; the result is **false** if the converted operand is **true**. The result is of type `bool`.  
  
 For an expression *e*, the unary expression **!***e* is equivalent to the expression **(***e* `==` 0), except where overloaded operators are involved.  
  
## Operator Keyword for !  
 The **not** operator is the text equivalent of **!**. There are two ways to access the **not** operator in your programs: include the header file `iso646.h`, or compile with the [/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md) (Disable language extensions) compiler option.  
  
## Example  
  
```  
// expre_Logical_NOT_Operator.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
  
int main() {  
   int i = 0;  
   if (!i)  
      cout << "i is zero" << endl;  
}  
```  
  
## See Also  
 [Expressions with Unary Operators](../vs140/Expressions-with-Unary-Operators.md)   
 [C++ Operators](../vs140/C---Operators.md)   
 [C++ Built-in Operators, Precedence and Associativity](../vs140/C---Built-in-Operators--Precedence-and-Associativity.md)   
 [Unary Arithmetic Operators](../vs140/Unary-Arithmetic-Operators.md)