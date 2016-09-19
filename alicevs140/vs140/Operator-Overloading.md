---
title: "Operator Overloading"
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
ms.assetid: 56ad4c4f-dd0c-45e0-adaa-08fe98cb1f8e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator Overloading
The `operator` keyword declares a function specifying what `operator-symbol` means when applied to instances of a class. This gives the operator more than one meaning, or "overloads" it. The compiler distinguishes between the different meanings of an operator by examining the types of its operands.  
  
## Syntax  
  
```  
  
type operator operator-symbol ( parameter-list )  
```  
  
## Remarks  
 You can redefine the function of most built-in operators globally or on a class-by-class basis. Overloaded operators are implemented as functions.  
  
 The name of an overloaded operator is `operator``x`, where `x` is the operator as it appears in the following table. For example, to overload the addition operator, you define a function called `operator+`. Similarly, to overload the addition/assignment operator, `+=`, define a function called `operator+=`.  
  
### Redefinable Operators  
  
|Operator|Name|Type|  
|--------------|----------|----------|  
|`,`|Comma|Binary|  
|`!`|Logical NOT|Unary|  
|`!=`|Inequality|Binary|  
|`%`|Modulus|Binary|  
|`%=`|Modulus assignment|Binary|  
|`&`|Bitwise AND|Binary|  
|`&`|Address-of|Unary|  
|`&&`|Logical AND|Binary|  
|`&=`|Bitwise AND assignment|Binary|  
|`( )`|Function call|—|  
|`( )`|Cast Operator|Unary|  
|`*`|Multiplication|Binary|  
|`*`|Pointer dereference|Unary|  
|`*=`|Multiplication assignment|Binary|  
|`+`|Addition|Binary|  
|`+`|Unary Plus|Unary|  
|`++`|Increment <sup>1</sup>|Unary|  
|`+=`|Addition assignment|Binary|  
|`–`|Subtraction|Binary|  
|`–`|Unary negation|Unary|  
|`––`|Decrement <sup>1</sup>|Unary|  
|`–=`|Subtraction assignment|Binary|  
|`–>`|Member selection|Binary|  
|`–>*`|Pointer-to-member selection|Binary|  
|`/`|Division|Binary|  
|`/=`|Division assignment|Binary|  
|`<`|Less than|Binary|  
|`<<`|Left shift|Binary|  
|`<<=`|Left shift assignment|Binary|  
|`<=`|Less than or equal to|Binary|  
|`=`|Assignment|Binary|  
|`==`|Equality|Binary|  
|`>`|Greater than|Binary|  
|`>=`|Greater than or equal to|Binary|  
|`>>`|Right shift|Binary|  
|`>>=`|Right shift assignment|Binary|  
|`[ ]`|Array subscript|—|  
|`^`|Exclusive OR|Binary|  
|`^=`|Exclusive OR assignment|Binary|  
|`&#124;`|Bitwise inclusive OR|Binary|  
|`&#124;=`|Bitwise inclusive OR assignment|Binary|  
|`&#124;&#124;`|Logical OR|Binary|  
|`~`|One's complement|Unary|  
|`delete`|`Delete`|—|  
|`new`|`New`|—|  
|`conversion operators`|conversion operators|Unary|  
  
 1   Two versions of the unary increment and decrement operators exist: preincrement and postincrement.  
  
 See [General Rules for Operator Overloading](../vs140/General-Rules-for-Operator-Overloading.md) for more information. The constraints on the various categories of overloaded operators are described in the following topics:  
  
-   [Unary Operators](../vs140/Overloading-Unary-Operators.md)  
  
-   [Binary Operators](../vs140/Binary-Operators.md)  
  
-   [Assignment](../vs140/Assignment.md)  
  
-   [Function Call](../vs140/Function-Call--C---.md)  
  
-   [Subscripting](../vs140/Subscripting.md)  
  
-   [Class-Member Access](../vs140/Member-Access.md)  
  
-   [Increment and Decrement](../vs140/Increment-and-Decrement-Operator-Overloading--C---.md).  
  
-   [Conversions](../vs140/User-Defined-Type-Conversions--C---.md)  
  
 The operators shown in the following table cannot be overloaded. The table includes the preprocessor symbols `#` and `##`.  
  
### Nonredefinable Operators  
  
|||  
|-|-|  
|`Operator`|`Name`|  
|`.`|Member selection|  
|`.*`|Pointer-to-member selection|  
|`::`|Scope resolution|  
|`? :`|Conditional|  
|`#`|Preprocessor convert to string|  
|`##`|Preprocessor concatenate|  
  
 Although overloaded operators are usually called implicitly by the compiler when they are encountered in code, they can be invoked explicitly the same way as any member or nonmember function is called:  
  
```  
Point pt;  
pt.operator+( 3 );  // Call addition operator to add 3 to pt.  
```  
  
## Example  
 The following example overloads the `+` operator to add two complex numbers and returns the result.  
  
```  
// operator_overloading.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
  
struct Complex {  
   Complex( double r, double i ) : re(r), im(i) {}  
   Complex operator+( Complex &other );  
   void Display( ) {   cout << re << ", " << im << endl; }  
private:  
   double re, im;  
};  
  
// Operator overloaded using a member function  
Complex Complex::operator+( Complex &other ) {  
   return Complex( re + other.re, im + other.im );  
}  
  
int main() {  
   Complex a = Complex( 1.2, 3.4 );  
   Complex b = Complex( 5.6, 7.8 );  
   Complex c = Complex( 0.0, 0.0 );  
  
   c = a + b;  
   c.Display();  
}  
```  
  
## Output  
  
```  
6.8, 11.2  
```  
  
## In this section  
  
1.  [General Rules for Operator Overloading](../vs140/General-Rules-for-Operator-Overloading.md)  
  
2.  [Overloading Unary Operators](../vs140/Overloading-Unary-Operators.md)  
  
3.  [Binary Operators](../vs140/Binary-Operators.md)  
  
4.  [Assignment](../vs140/Assignment.md)  
  
5.  [Function Call (C++)](../vs140/Function-Call--C---.md)  
  
6.  [Subscripting](../vs140/Subscripting.md)  
  
7.  [Member Access](../vs140/Member-Access.md)  
  
## See Also  
 [C++ Operators](../vs140/C---Operators.md)   
 [Keywords](../vs140/Keywords--C---.md)