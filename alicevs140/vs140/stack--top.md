---
title: "stack::top"
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
ms.topic: article
ms.assetid: d5b36f82-7d9d-40f8-ad81-429507daa691
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# stack::top
Returns a reference to an element at the top of the stack.  
  
## Syntax  
  
```  
reference top( );  
const_reference top( ) const;  
```  
  
## Return Value  
 A reference to the last element in the container at the top of the stack.  
  
## Remarks  
 The stack must be nonempty to apply the member function. The top of the stack is the position occupied by the most recently added element and is the last element at the end of the container.  
  
 If the return value of **top** is assigned to a `const_reference`, the stack object cannot be modified. If the return value of **top** is assigned to a **reference**, the stack object can be modified.  
  
## Example  
  
```  
// stack_top.cpp  
// compile with: /EHsc  
#include <stack>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   stack <int> s1;  
  
   s1.push( 1 );  
   s1.push( 2 );  
  
   int& i = s1.top( );  
   const int& ii = s1.top( );  
  
   cout << "The top integer of the stack s1 is "  
        << i << "." << endl;  
   i--;  
   cout << "The next integer down is "<< ii << "." << endl;  
}  
```  
  
 **The top integer of the stack s1 is 2.**  
**The next integer down is 1.**   
## Requirements  
 **Header:** <stack\>  
  
 **Namespace:** std  
  
## See Also  
 [stack Class](../vs140/stack-Class.md)   
 [stack::top and stack::empty](../vs140/stack--top-and-stack--empty.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)