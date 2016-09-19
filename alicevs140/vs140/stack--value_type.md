---
title: "stack::value_type"
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
ms.assetid: 7d974141-e2eb-4b6c-8ba3-ecdedb581a32
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# stack::value_type
A type that represents the type of object stored as an element in a stack.  
  
## Syntax  
  
```  
typedef typename Container::value_type value_type;  
```  
  
## Remarks  
 The type is a synonym for `value_type` of the base container adapted by the stack.  
  
## Example  
  
```  
// stack_value_type.cpp  
// compile with: /EHsc  
#include <stack>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   // Declares stacks with default deque base container  
   stack<int>::value_type AnInt;  
  
   AnInt = 69;  
   cout << "The value_type is AnInt = " << AnInt << endl;  
  
   stack<int> s1;  
   s1.push( AnInt );  
   cout << "The element at the top of the stack is "  
        << s1.top( ) << "." << endl;  
}  
```  
  
 **The value_type is AnInt = 69**  
**The element at the top of the stack is 69.**   
## Requirements  
 **Header:** <stack\>  
  
 **Namespace:** std  
  
## See Also  
 [stack Class](../vs140/stack-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)