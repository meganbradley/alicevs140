---
title: "deque::pop_front"
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
ms.assetid: dfc3008e-1ea4-4984-9cd4-38e8b37ffca3
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# deque::pop_front
Deletes the element at the beginning of the deque.  
  
## Syntax  
  
```  
  
void pop_front( );  
  
```  
  
## Remarks  
 The first element must not be empty. `pop_front` never throws an exception.  
  
## Example  
  
```  
// deque_pop_front.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1;  
  
   c1.push_back( 1 );  
   c1.push_back( 2 );  
   cout << "The first element is: " << c1.front( ) << endl;  
   cout << "The second element is: " << c1.back( ) << endl;  
  
   c1.pop_front( );  
   cout << "After deleting the element at the beginning of the "  
      "deque, the first element is: " << c1.front( ) << endl;  
}  
```  
  
 **The first element is: 1**  
**The second element is: 2**  
**After deleting the element at the beginning of the deque, the first element is: 2**   
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [deque::push_front and deque::pop_front](../vs140/deque--push_front-and-deque--pop_front.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)