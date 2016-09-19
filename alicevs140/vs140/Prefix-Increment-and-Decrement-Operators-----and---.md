---
title: "Prefix Increment and Decrement Operators: ++ and --"
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
ms.assetid: 45ea7fc7-f279-4be9-a216-1d9a0ef9eb7b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Prefix Increment and Decrement Operators: ++ and --
## Syntax  
  
```  
  
      ++ unary-expression  
–– unary-expression  
```  
  
## Remarks  
 The prefix increment operator (`++`) adds one to its operand; this incremented value is the result of the expression. The operand must be an l-value not of type **const**. The result is an l-value of the same type as the operand.  
  
 The prefix decrement operator (**––**) is analogous to the prefix increment operator, except that the operand is decremented by one and the result is this decremented value.  
  
 Both the prefix and postfix increment and decrement operators affect their operands. The key difference between them is the order in which the increment or decrement takes place in the evaluation of an expression. (For more information, see [Postfix Increment and Decrement Operators](../vs140/Postfix-Increment-and-Decrement-Operators-----and---.md).) In the prefix form, the increment or decrement takes place before the value is used in expression evaluation, so the value of the expression is different from the value of the operand. In the postfix form, the increment or decrement takes place after the value is used in expression evaluation, so the value of the expression is the same as the value of the operand. For example, the following program prints "`++i = 6`":  
  
```  
// expre_Increment_and_Decrement_Operators.cpp  
// compile with: /EHsc  
#include <iostream>  
  
using namespace std;  
  
int main() {  
   int i = 5;  
   cout << "++i = " << ++i << endl;  
}  
```  
  
 An operand of integral or floating type is incremented or decremented by the integer value 1. The type of the result is the same as the operand type. An operand of pointer type is incremented or decremented by the size of the object it addresses. An incremented pointer points to the next object; a decremented pointer points to the previous object.  
  
 Because increment and decrement operators have side effects, using expressions with increment or decrement operators in a [preprocessor macro](../vs140/Macros--C-C---.md) can have undesirable results. Consider this example:  
  
```  
// expre_Increment_and_Decrement_Operators2.cpp  
#define max(a,b) ((a)<(b))?(b):(a)  
  
int main()  
{  
   int i = 0, j = 0, k;  
   k = max( ++i, j );  
}  
```  
  
 The macro expands to:  
  
```  
k = ((++i)<(j))?(j):(++i);  
```  
  
 If `i` is greater than or equal to `j` or less than `j` by 1, it will be incremented twice.  
  
> [!NOTE]
>  C++ inline functions are preferable to macros in many cases because they eliminate side effects such as those described here, and allow the language to perform more complete type checking.  
  
## See Also  
 [Expressions with Unary Operators](../vs140/Expressions-with-Unary-Operators.md)   
 [C++ Operators](../vs140/C---Operators.md)   
 [C++ Built-in Operators, Precedence and Associativity](../vs140/C---Built-in-Operators--Precedence-and-Associativity.md)   
 [Prefix Increment and Decrement Operators](../vs140/Prefix-Increment-and-Decrement-Operators.md)