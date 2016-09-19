---
title: "deque::reference"
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
ms.assetid: 3ee66c66-497c-4546-bf07-4c3ebc37df26
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# deque::reference
A type that provides a reference to an element stored in a deque.  
  
## Syntax  
  
```  
  
typedef typename Allocator::reference reference;  
  
```  
  
## Example  
  
```  
// deque_reference.cpp  
// compile with: /EHsc  
#include <deque>  
#include <iostream>  
  
int main( )   
{  
   using namespace std;  
   deque <int> c1;  
  
   c1.push_back( 10 );  
   c1.push_back( 20 );  
  
   const int &i = c1.front( );  
   int &j = c1.back( );  
   cout << "The first element is " << i << endl;  
   cout << "The second element is " << j << endl;  
}  
```  
  
 **The first element is 10**  
**The second element is 20**   
## Requirements  
 **Header:** <deque\>  
  
 **Namespace:** std  
  
## See Also  
 [deque Class](../vs140/deque-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)