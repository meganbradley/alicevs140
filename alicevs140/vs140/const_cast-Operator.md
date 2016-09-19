---
title: "const_cast Operator"
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
ms.assetid: 4d8bb203-ef33-4a10-9f9f-c64d4fbc1687
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# const_cast Operator
Removes the **const**, `volatile`, and **__unaligned** attribute(s) from a class.  
  
## Syntax  
  
```  
  
const_cast <   
type-id  
 > (   
expression  
 )  
  
```  
  
## Remarks  
 A pointer to any object type or a pointer to a data member can be explicitly converted to a type that is identical except for the **const**, `volatile`, and **__unaligned** qualifiers. For pointers and references, the result will refer to the original object. For pointers to data members, the result will refer to the same member as the original (uncast) pointer to data member. Depending on the type of the referenced object, a write operation through the resulting pointer, reference, or pointer to data member might produce undefined behavior.  
  
 You cannot use the `const_cast` operator to directly override a constant variable's constant status.  
  
 The `const_cast` operator converts a null pointer value to the null pointer value of the destination type.  
  
## Example  
  
```  
// expre_const_cast_Operator.cpp  
// compile with: /EHsc  
#include <iostream>  
  
using namespace std;  
class CCTest {  
public:  
   void setNumber( int );  
   void printNumber() const;  
private:  
   int number;  
};  
  
void CCTest::setNumber( int num ) { number = num; }  
  
void CCTest::printNumber() const {  
   cout << "\nBefore: " << number;  
   const_cast< CCTest * >( this )->number--;  
   cout << "\nAfter: " << number;  
}  
  
int main() {  
   CCTest X;  
   X.setNumber( 8 );  
   X.printNumber();  
}  
```  
  
 On the line containing the `const_cast`, the data type of the `this` pointer is `const CCTest *`. The `const_cast` operator changes the data type of the `this` pointer to `CCTest *`, allowing the member `number` to be modified. The cast lasts only for the remainder of the statement in which it appears.  
  
## See Also  
 [Casting Operators](../vs140/Casting-Operators.md)   
 [Keywords](../vs140/Keywords--C---.md)