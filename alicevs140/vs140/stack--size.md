---
title: "stack::size"
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
ms.assetid: 46e271c4-7214-41b3-a72b-77687447e99c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# stack::size
Returns the number of elements in the stack.  
  
## Syntax  
  
```  
  
size_type size( ) const;  
  
```  
  
## Return Value  
 The current length of the stack.  
  
## Example  
  
```  
// stack_size.cpp  
// compile with: /EHsc  
#include <stack>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   stack <int> s1, s2;  
   stack <int>::size_type i;  
  
   s1.push( 1 );  
   i = s1.size( );  
   cout << "The stack length is " << i << "." << endl;  
  
   s1.push( 2 );  
   i = s1.size( );  
   cout << "The stack length is now " << i << "." << endl;  
}  
```  
  
 **The stack length is 1.**  
**The stack length is now 2.**   
## Requirements  
 **Header:** <stack\>  
  
 **Namespace:** std  
  
## See Also  
 [stack Class](../vs140/stack-Class.md)   
 [stack::size](../vs140/stack--size--STL-Samples-.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)