---
title: "Lvalues and Rvalues (Visual C++)"
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
ms.assetid: a8843344-cccc-40be-b701-b71f7b5cdcaf
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Lvalues and Rvalues (Visual C++)
Every C++ expression is either an lvalue or an rvalue. An lvalue refers to an object that persists beyond a single expression. You can think of an lvalue as an object that has a name. All variables, including nonmodifiable (`const`) variables, are lvalues. An rvalue is a temporary value that does not persist beyond the expression that uses it. To better understand the difference between lvalues and rvalues, consider the following example:  
  
```  
// lvalues_and_rvalues1.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
int main()  
{  
   int x = 3 + 4;  
   cout << x << endl;  
}  
```  
  
 In this example, `x` is an lvalue because it persists beyond the expression that defines it. The expression `3 + 4` is an rvalue because it evaluates to a temporary value that does not persist beyond the expression that defines it.  
  
 The following example demonstrates several correct and incorrect usages of lvalues and rvalues:  
  
```  
// lvalues_and_rvalues2.cpp  
int main()  
{  
   int i, j, *p;  
  
   // Correct usage: the variable i is an lvalue.  
   i = 7;  
  
   // Incorrect usage: The left operand must be an lvalue (C2106).  
   7 = i; // C2106  
   j * 4 = 7; // C2106  
  
   // Correct usage: the dereferenced pointer is an lvalue.  
   *p = i;   
  
   const int ci = 7;  
   // Incorrect usage: the variable is a non-modifiable lvalue (C3892).  
   ci = 9; // C3892  
  
   // Correct usage: the conditional operator returns an lvalue.  
   ((i < 3) ? i : j) = 7;  
}  
```  
  
> [!NOTE]
>  The examples in this topic illustrate correct and incorrect usage when operators are not overloaded. By overloading operators, you can make an expression such as `j * 4` an lvalue.  
  
 The terms *lvalue* and *rvalue* are often used when you refer to object references. For more information about references, see [Lvalue Reference Declarator: &](../vs140/Lvalue-Reference-Declarator---.md) and [Rvalue Reference Declarator: &&](../vs140/Rvalue-Reference-Declarator----.md).  
  
## See Also  
 [Basic Concepts](../vs140/Basic-Concepts---C---.md)   
 [Lvalue Reference Declarator: &](../vs140/Lvalue-Reference-Declarator---.md)   
 [Rvalue Reference Declarator: &&](../vs140/Rvalue-Reference-Declarator----.md)