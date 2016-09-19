---
title: "Address-of Operator: &amp;"
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
ms.assetid: 2828221a-15f6-4acc-87fe-25e34feebb88
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Address-of Operator: &amp;
## Syntax  
  
```  
  
& cast-expression  
```  
  
## Remarks  
 The unary address-of operator (**&**) takes the address of its operand. The operand of the address-of operator can be either a function designator or an l-value that designates an object that is not a bit field and is not declared with the **register** storage-class specifier.  
  
 The address-of operator can only be applied to variables with fundamental, structure, class, or union types that are declared at the file-scope level, or to subscripted array references. In these expressions, a constant expression that does not include the address-of operator can be added to or subtracted from the address-of expression.  
  
 When applied to functions or l-values, the result of the expression is a pointer type (an r-value) derived from the type of the operand. For example, if the operand is of type `char`, the result of the expression is of type pointer to `char`. The address-of operator, applied to **const** or `volatile` objects, evaluates to **const** `type` **\*** or `volatile` `type` **\***, where `type` is the type of the original object.  
  
 When the address-of operator is applied to a [qualified name](assetId:///3fefb16d-8120-4627-8b3f-3d90fbdcd1df), the result depends on whether the *qualified-name* specifies a static member. If so, the result is a pointer to the type specified in the declaration of the member. If the member is not static, the result is a pointer to the member *name* of the class indicated by *qualified-class-name*. (See [Primary Expressions](../vs140/Primary-Expressions.md) for more about *qualified-class-name*.) The following code fragment shows how the result differs, depending on whether the member is static:  
  
```  
// expre_Address_Of_Operator.cpp  
// C2440 expected  
class PTM {  
public:  
           int   iValue;  
    static float fValue;  
};  
  
int main() {  
   int   PTM::*piValue = &PTM::iValue;  // OK: non-static  
   float PTM::*pfValue = &PTM::fValue;  // C2440 error: static  
   float *spfValue     = &PTM::fValue;  // OK  
}  
```  
  
 In this example, the expression `&PTM::fValue` yields type `float *` instead of type `float PTM::*` because `fValue` is a static member.  
  
 The address of an overloaded function can be taken only when it is clear which version of the function is being referenced. See [Address of Overloaded Functions](../vs140/Address-of-Overloaded-Functions.md) for information about how to obtain the address of a particular overloaded function.  
  
 Applying the address-of operator to a reference type gives the same result as applying the operator to the object to which the reference is bound. For example:  
  
## Example  
  
```  
// expre_Address_Of_Operator2.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
int main() {  
   double d;        // Define an object of type double.  
   double& rd = d;  // Define a reference to the object.  
  
   // Obtain and compare their addresses  
   if( &d == &rd )  
      cout << "&d equals &rd" << endl;  
}  
```  
  
## Output  
  
```  
&d equals &rd  
```  
  
 The following example uses the address-of operator to pass a pointer argument to a function:  
  
```  
// expre_Address_Of_Operator3.cpp  
// compile with: /EHsc  
// Demonstrate address-of operator &  
  
#include <iostream>  
using namespace std;  
  
// Function argument is pointer to type int  
int square( int *n ) {  
   return (*n) * (*n);  
}  
  
int main() {  
   int mynum = 5;  
   cout << square( &mynum ) << endl;   // pass address of int  
}  
```  
  
## Output  
  
```  
25  
```  
  
## See Also  
 [Expressions with Unary Operators](../vs140/Expressions-with-Unary-Operators.md)   
 [C++ Operators](../vs140/C---Operators.md)   
 [C++ Built-in Operators, Precedence and Associativity](../vs140/C---Built-in-Operators--Precedence-and-Associativity.md)   
 [Lvalue Reference Declarator: &](../vs140/Lvalue-Reference-Declarator---.md)   
 [Indirection and Address-of Operators](../vs140/Indirection-and-Address-of-Operators.md)