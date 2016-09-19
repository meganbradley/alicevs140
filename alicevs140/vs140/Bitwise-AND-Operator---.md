---
title: "Bitwise AND Operator: &amp;"
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
ms.assetid: 76f40de3-c417-47b9-8a77-532f3fc990a5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Bitwise AND Operator: &amp;
## Syntax  
  
```  
  
expression   
&  
 expression  
  
```  
  
## Remarks  
 The expressions may be other and-expressions, or (subject to the type restrictions mentioned below) equality expressions, relational expressions, additive expressions, multiplicative expressions, pointer to member expressions, cast expressions, unary expressions, postfix expressions, or primary expressions.  
  
 The bitwise AND operator (**&**) compares each bit of the first operand to the corresponding bit of the second operand. If both bits are 1, the corresponding result bit is set to 1. Otherwise, the corresponding result bit is set to 0.  
  
 Both operands to the bitwise AND operator must be of integral types. The usual arithmetic conversions covered in [Arithmetic Conversions](../vs140/Arithmetic-Conversions.md), are applied to the operands.  
  
## Operator Keyword for &  
 The `bitand` operator is the text equivalent of **&**. There are two ways to access the `bitand` operator in your programs: include the header file `iso646.h`, or compile with the [/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md) (Disable language extensions) compiler option.  
  
## Example  
  
```  
// expre_Bitwise_AND_Operator.cpp  
// compile with: /EHsc  
// Demonstrate bitwise AND  
#include <iostream>  
using namespace std;  
int main() {  
   unsigned short a = 0xFFFF;      // pattern 1111 ...  
   unsigned short b = 0xAAAA;      // pattern 1010 ...  
  
   cout  << hex << ( a & b ) << endl;   // prints "aaaa", pattern 1010 ...  
}  
```  
  
## See Also  
 [C++ Bitwise Operators](../vs140/C---Bitwise-Operators.md)   
 [C++ Operators](../vs140/C---Operators.md)   
 [C++ Built-in Operators, Precedence and Associativity](../vs140/C---Built-in-Operators--Precedence-and-Associativity.md)   
 [C Bitwise Operators](../vs140/C-Bitwise-Operators.md)