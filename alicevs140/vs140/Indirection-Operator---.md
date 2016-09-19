---
title: "Indirection Operator: *"
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
ms.assetid: c50309e1-6c02-4184-9fcb-2e13c1f4ac03
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Indirection Operator: *
## Syntax  
  
```  
  
* cast-expression  
```  
  
## Remarks  
 The unary indirection operator (**\***) dereferences a pointer; that is, it converts a pointer value to an l-value. The operand of the indirection operator must be a pointer to a type. The result of the indirection expression is the type from which the pointer type is derived. The use of the **\*** operator in this context is different from its meaning as a binary operator, which is multiplication.  
  
 If the operand points to a function, the result is a function designator. If it points to a storage location, the result is an l-value designating the storage location.  
  
 The indirection operator may be used cumulatively to dereference pointers to pointers. For example:  
  
```  
// expre_Indirection_Operator.cpp  
// compile with: /EHsc  
// Demonstrate indirection operator  
#include <iostream>  
using namespace std;  
int main() {  
   int n = 5;  
   int *pn = &n;  
   int **ppn = &pn;  
  
   cout  << "Value of n:\n"  
         << "direct value: " << n << endl  
         << "indirect value: " << *pn << endl  
         << "doubly indirect value: " << **ppn << endl  
         << "address of n: " << pn << endl  
         << "address of n via indirection: " << *ppn << endl;  
}  
```  
  
 If the pointer value is invalid, the result is undefined. The following list includes some of the most common conditions that invalidate a pointer value.  
  
-   The pointer is a null pointer.  
  
-   The pointer specifies the address of a local item that is not visible at the time of the reference.  
  
-   The pointer specifies an address that is inappropriately aligned for the type of the object pointed to.  
  
-   The pointer specifies an address not used by the executing program.  
  
## See Also  
 [Expressions with Unary Operators](../vs140/Expressions-with-Unary-Operators.md)   
 [C++ Operators](../vs140/C---Operators.md)   
 [C++ Built-in Operators, Precedence and Associativity](../vs140/C---Built-in-Operators--Precedence-and-Associativity.md)   
 [Address-of Operator: &](../vs140/Address-of-Operator---.md)   
 [Indirection and Address-of Operators](../vs140/Indirection-and-Address-of-Operators.md)